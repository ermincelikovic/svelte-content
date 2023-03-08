# Svelte Content
So far this just an idea. Svelte Content should be the most lightweight and straight-forward content management library for svelte kit.

## Goals
- Takes less than 3 minutes to drop it into the project
- Minimum amount of configuration steps - ideally less than 3
- The most basic setup does NOT require neither external database server nor user-run migrations
- UI for the content management 
  
## Installation steps concept
1. npm install svelte-content
2. Some one-liner somewhere in the codebase
3. Add Prisma's db connection string into .env (initially sqlite, so the extenral service is not necessary)
4. Done - access the interface via website.com/sc

Make sure there is a basic auth implemented, probably auth.js, or simply define usr/pwd through the .env

## Usage in layouts
I'm not completely sure how to handle this, but I have couple of ideas
- Treat it as a global store, call it sc - sprinkle custom functions on top
- Figure out how to make it as a globally avilable prop, and somehow connect which route should receive which content

## Content editing
The content editing part should be in a form of a sidebar which could be floating over the app. I don't think that, for now, it should have it's separate page.  
  
Visiting website.com/sc will trigger the sidebar on homepage (probably by redirecting back to homepage with certain headers)