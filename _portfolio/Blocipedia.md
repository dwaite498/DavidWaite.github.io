---
layout: post
title: Blocipedia
feature-img: "img/Blocipedia_sample.png"
thumbnail-path: "img/Blocipedia_sample.png"
short-description: Blocipedia is a wiki creation and collaboration app.

---

Blocipedia
-------

Bocipedia is a project that was a part of the Bloc curriculum that was used to gain experience with creating users, interacting with CRUD actions,
adressing authorization concerns, and changing user access based on different situations.

There are photos and a write up on the project here: [Blocipedia Repo](https://github.com/dwaite498/blocipedia-2)

Explanation
-----
I created this project with minimal provided code from Bloc. I had several coding mentors who assisted me throughout the process.

The situation surrounding this project is that a client wanted an app that would allow users to create both paid and free accounts with which to collaborate
on editable wiki pages. The client requested admin access to all posted wikis, private and public, and the ability to curate them as necessary for content.

Learning OUtcomes
-----
This was my first larger project with the Ruby on Rails framework. Up to this point all of my Rails projects had been small, guided apps that taught one small part of
the framework. This brought it all together. In this app the one part that I learned that I did not have much ofany understanding of before hand, as user validation.
This was the first project that I had to think about who could access what, and what ways could they go around the limits. Up until this point I had just used hiding
my links and buttons with basic inline user role queries:
```
<% if user.Admin? %>
  <p><%= link_to wiki.title, wiki %></p>
<% end %>
    
```
In this project I added validations in the model that would restrict user  access based on who they were and where in thewebsite they were allowed regardless of how they got there.
The entire website required a user to exist to see any content. If a user signed in, they had limited access until they upgraded to a premium account, and the admins could
go anywhere they wanted to keep an eye on content wether they were invited to a private wiki or not.