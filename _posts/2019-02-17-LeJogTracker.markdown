---
layout: post
title:  "LeJog Tracker"
date:   2018-08-03 15:00:00
categories: jekyll update
---

# Land's End to John O Groats tracker.

This app allows users to track their virtual progress from Land's end to John O Groats on a google map.

I'm using Ruby on rails for the app, and the front end employs some React jsx for the map view and the leader board.  GPX files are XML and I load the coordinates by AJAX and plot them on the map, along with the leader positions are loaded dynamically in the same way.

The tech stack is Ruby 2.4.0 Rails 5.1.6 Postgresql. Resque (for background jobs).  I'm using the background jobs to collect the data so it is ready for the user to see at any time.  Services running are: Resque, resque worker, resque scheduler.

The strava auth controller stores athlete authorisation tokens and athlete refresh tokens in the users table.
There is a refresh tokens job that queues a refresh token jon for each user at 10 second intervals.

I use the strava webhook. This posts data to this application when a signed up user creates a run. It then uses the strava data API to populate the data for that run.

I am hosting this website on a Digital Ocean Droplet.  I enjoyed setting this up from a bare bones linux distribution, e.g. installing ruby, postgres, nginx, etc and setting up my web address to point to it.

At the moment, I have a problem in that Strava deny me access to user data when the user is not connected with the API owner, I am working on this.

[It is hosted here](https://eastleighlejogtracker.co.uk/)
