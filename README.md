    |--------------------------------------------------------------------------|
    |--------------------------Co/\/\p|_|T3R----$c13nc3------------------------|
    |--------------------------------------------------------------------------| 
    |     _________                    AAA                                     |
    |    mmmmmmmmmmmm   _____         AAAAA                    @AresDevelopment|
    |   mm    mm    mm  rrrrr        AA   AA                                   |
    |   mm    mm    mm  rr          AAAAAAAAA                                  |
    |   mm    mm    mm  rr   _._   AAA     AAA (and his much smarter students!)|
    |--------------------------------------------------------------------------|
    |--------------------------------------------------------------------------|

### Summary of Process
1. Start a Rails environment in c9
2. Change Gemfile so sqlite3 and pg are in the right groups
    1. https://www.udemy.com/the-complete-ruby-on-rails-developer-course/learn/v4/t/lecture/3850160?start=0
    2. `bundle install --without production`
3. Initilize github and push to a repo
    1. Setup SSH keys so I don't have to keep entering passwords
4. heroku
    5. `heroku create`
    6. `heroku keys:add`
    7. `git push heroku master`
    8. `git remote rm heroku` (There's an easier way of changing heroku names)
    9. `heroku git:remote -a ares-development`
5. Hello World
    1. Uncommented the root route
    2. created `app/controllers/welcome_controller.rb`
    3. created `app/views/welcome/index.html.erb`
    4. Deploy to heroku and setup to auto deploy master branch
6. Devise
    1. add `gem 'devise'` to Gemfile
    2. `bundle install --without production`
    3. `rails generate devise:install`
    4. `rails generate devise User`
    5. `rake db:migrate`
    6. add `before_action :authenticate_user!` to `application_controller.rb` <-- requires all users to login
    7. `rake routes | grep user` -- See the routes built? Now you can add links like:
    8. `<%= link_to "logout", destroy_user_session_path, method: :delete %>`
7. Bootstrap + Devise
    1. Add `gem 'twitter-bootstrap-rails'`
    2. `rails generate bootstrap:install static`
    3. `rails g bootstrap:layout application`
    4. `bundle install --without production`
    5. Add `gem 'devise-bootstrap-views'` to Gemfile
    6. `bundle install --without production`
    7. Add `*= require devise_bootstrap_views` to `app/assets/stylesheets/application.css`
    8. `rails g devise:views:locale en` (something didn't work the same as demo)
    9. `rails g devise:views:bootstrap_templates`
    10. Make sure `devise_for :users` is in routes file