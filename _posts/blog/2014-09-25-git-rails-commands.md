---
layout: post
title: "Git, Rails дээр байнга хэрэглэгддэг командууд"
modified: 2014-09-27 20:20:37
categories: blog
excerpt:
tags: []
image:
  feature:
date: 2014-09-25 17:26:48
comments: true
share: true
---
Байнга хэрэглэгддэг командуудыг дараа нь харж байхад амар учир энд хадгалахаар шийдлээ. 

{% highlight shell %}
git init
git add -A
git commit -m "message"
git commit -am "message"
git remote add origin gitaddress.git
git push -u origin --all
git checkout -b mybranch
git push -u origin mybranch
git push
git checkout master
git merge mybranch
heroku create
git push heroku master
git push heroku
git remote -v
heroku logs
heroku git:remote -a appname
heroku git:remote -a appname -r other_remote_name
heroku config:set AABB=aabb
heroku config
rails new appname
rails g controller MyCont cont1 cont2
rails destroy controller MyCont cont1 cont2
rails g model User name:string email:string
rails destroy model User
rake db:migrate
rake db:migrate:reset
rake db:rollback
rake db:migrate VERSION=0 #rollback to beginning of time kk
rake db:seed
rake test
rake test:prepare
bundle exec rake test #force
bundle install --without production
{% endhighlight %}