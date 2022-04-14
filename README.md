# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

Steps:
- $ rails new hello-world -d postgresql -T
- $ cd hello-world
- $ rails db:create
- $ rails s
- $ bundle add webpacker
- $ bundle add react-rails
- $ rails webpacker:install
- $ rails webpacker:install:react
- $ yarn add @babel/preset-react
- $ yarn add @rails/activestorage
- $ yarn add @rails/ujs
- $ rails generate react:install
- $ rails generate react:component App
- Copy pasted Syllabus code to App.js
- $ rails generate controller Home
-  Add index.html.erb file app/views/home
- Delete  <%= javascript_importmap_tags %> replace <%= javascript_pack_tag 'application', 'data-turbolinks-track': 'reload' %>
- routes.rb add root 'home#index'
- $ bundle add bootstrap
- $ mv app/assets/stylesheets/application.css app/assets/stylesheets/application.scss
- $ yarn add reactstrap
- assets/stylesheets/application.scss add @import 'bootstrap';
- Add Assets, Components, Pages in appropriate folders at App.js then add boiler plates on each
- Add $ yarn add react-router-dom@5.3.0
- In App.js add import {
  BrowserRouter as  Router,
  Route,
  Switch
} from 'react-router-dom'

import Navigation from './components/Navigation'
import AboutUs from './pages/AboutUs'
import Home from './pages/Home'
- Replace Hello World to router tags:
<Router>
  <Navigation />
  <Switch>
    <Route exact path="/" component={Home} />
    <Route path="/about" component={AboutUs} />
  </Switch>
</Router>
- In routes.rb add $ get '*path', to: 'home#index', constraints: ->(request){ request.format.html? }
- In Navigation.js add import React, { Component } from 'react'
import { Nav, NavItem } from 'reactstrap'
import { NavLink } from 'react-router-dom'

class Navigation extends Component {
  render() {
    return(
      <>
        <Nav>
          <NavItem>
            <NavLink to="/" className="nav-link">Home</NavLink>
          </NavItem>
          <NavItem>
            <NavLink to="/about" className="nav-link">About Us</NavLink>
          </NavItem>
        </Nav>
      </>
    )
  }
}
export default Navigation
- 