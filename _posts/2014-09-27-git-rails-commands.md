---
layout: post
title: "Git, Rails дээр байнга хэрэглэгддэг командууд"
description: "Байнга хэрэглэгддэг командуудыг дараа нь харж байхад амар учир энд хадгалахаар шийдлээ. "
comment: yes
---

Байнга хэрэглэгддэг командуудыг дараа нь харж байхад амар учир энд хадгалахаар шийдлээ. 

###Git commands

Гит дөнгөж эхлэж байхад байнга ямар команд хэрэглэхээ мартах явдал их гардаг шүү дээ. Өөртөө зориулж гаргасан жагсаалт маань. 

    # Суулгасны дараах анхны тохиргоо, нэр имэйл
    git config --global user.name "Name Name"
    git config --global user.email "email@mail.com"
    git config --list
    #
    git config --global alias.co checkout
    git init
    git add -A
    git commit -m "message"
    git commit -am "message"
    git remote add origin gitaddress.git
    git push -u origin --all
    git checkout -b mybranch
    git branch --color
    git push -u origin mybranch
    git branch -d mybranch #delete branch
    git push
    git checkout master
    git merge mybranch


### Git ба Heroku

heroku дээр ажиллахад хэрэгтэй хэсэг
    
    heroku create
    git push heroku master
    git push heroku
    git remote -v
    heroku logs
    # хуучин байсан төсөл дээр heroku нэмэх
    heroku git:remote -a appname
    heroku git:remote -a appname -r other_remote_name
    heroku config:set AABB=aabb
    heroku config

### Rails commands


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