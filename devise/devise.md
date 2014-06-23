## Devise Notes

**Initial Setup/Install**

1) Add `gem 'devise'`

2)  Install Devise with `rails generate devise:install`

3) Add `config.action_mailer.default_url_options = { :host => 'localhost:3000' }` to config/environments/development.rb

4) Add `config.action_mailer.default_url_options = { :host => 'http://blahbla....' }` to config/environments/production.rb

5) Add the following flash messages to application.html.erb
```
<% flash.each do |name, msg| %>
     <%= content_tag(:div, msg, class: "alert alert-info") %>
<% end %>
```

6) In config/application.rb, add `config.assets.initialize_on_precompile = false`

7) Install Devise views with `$ rails g devise:views`

**Generate Users**

1) `rails generate devise user`

2) Migrate your database: `rake db:migrate`

3) Restart server
