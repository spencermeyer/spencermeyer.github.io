---
layout: post
title:  "RubyScraper"
date:   2018-08-03 15:00:00
categories: jekyll update
---

My Land's End to John O Groats tracker. .......................................

This app allows users to track their virtual progress from Land's end to John O Groats on a google map.

I'm using Ruby on rails for the app, and the front end employs some React jsx for the map view.

Ruby 2.4.0 Rails 5.1.6 Postgresql. Resque (for background jobs).

Services running are: Resque, resque worker, resque scheduler.

The strava auth controller stores athlete authorisation tokens and athlete refresh tokens in the users table.
There is a refresh tokens job that queues a refresh token jon for each user at 10 second intervals.

I use the strava webhook. This posts data to this application when a signed up user creates a run. It then uses the strava data API to populate the data for that run.
