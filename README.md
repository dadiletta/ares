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