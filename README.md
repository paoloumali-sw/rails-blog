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

## Deploying to Heroku

- $ ``gem install bundler``
- First [download OpenSSL](https://bintray.com/oneclick/OpenKnapsack/download_file?file_path=x86%2Fopenssl-1.0.2j-x86-windows.tar.lzma). Next, extract the lzma download with 7Zip, and then extract the tar file to C:\openssl.
- [download heroku cli](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)
- $ heroku login
- $ heroku apps:create {nameOfApp}

## Todos
* How to run the test suite
* Services (job queues, cache servers, search engines, etc.)