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

a) Niveau facile
- Album.count => 347
- song = Track.find_by(title: "White Room") => Eric Capton
- duration = Track.find_by(duration: 188133) => Perfect
- group = Album.find_by(title: "Use Your Illusion II") => Gun and Roses

b) Niveau Moyen
- alb = Album.where("title like?", "%Great%") alb.count = 13
- al = Album.where("title like?", "%music%") al.destroy_all
- acdc = Album.where(artist: 'AC/DC') acdc.count
- song = Track.where(duration: 158589) song.count

c) Niveau Difficile
- acdc = Track.where(artist: "AC/DC")  acdc.each {|song| puts "voici les titres de AC/DC: #{song.title}"}
- titre = Track.where(album: "let machin")titre.each {|song| puts "voici les titre de l'album Let machin : #{song.title}"}
- title_price = titre.map {|line| line.price} title_price.sum  title_duration = titre.map{|line| line.duration}.sum
- dp = Track.where(artist: "Deep Purple")  dp_price = dp.map{|line| line.price}.sum
-  bs = Track.where(artist: "Eric Clapton") britney_spears = bs.each{|song| song.update(artist: "Britney Spears")} 
