# README

Setup summary can be found here: https://gist.github.com/paoloumali-sw/b144bac45323242202641c4cd82fb64d

## Info
* Ruby version: 2.5.5p157
* Rails version: 5.2.3
* System dependencies: Windows 10 Pro
* Database: MySQL

## Setup

- clone this repo
- create your databases, see Databases section
- try if app can connect to db, $ ``rails db:schema:dump``. It works if db/schema.rb is created
- see Serve project section

## Databases

```sql
CREATE DATABASE rails_blog_dev;
CREATE DATABASE rails_blog_test;
CREATE USER 'rails_user'@'localhost' IDENTIFIED BY 'secret';
GRANT ALL PRIVILEGES ON rails_blog_dev.* TO `rails_user`@`localhost`;
GRANT ALL PRIVILEGES ON rails_blog_test.* TO `rails_user`@`localhost`;
FLUSH PRIVILEGES;
```

## Serve project

- $ ``rails server``. Puma will serve app to something like: http://localhost:3000

## Todos
* How to run the test suite
* Services (job queues, cache servers, search engines, etc.)
* Deployment instructions