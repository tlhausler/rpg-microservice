# Java Microservices Project

## Context

This is the final project for my web services class.  I was tasked with creating a microservices project, but what the services handled were up to me.  I deciced to continue with the tabletop rpg theme and this time create a tool for dungeon masters to keep track of the games they run, which players are in them, and the equipment those players' characters have.  

## Action

Using Spring Initializr, I created all five microservices needed for the project.  Dependencies used were Lombok, Spring Data JPA, Spring Web, H2 Database, Eureka Server, Eurkea Discovery Client, and Gateway.  A registry service was made with Eureka Server to keep track of all services and their health on the server.  A gateway service was implemented to route all traffick through a single port and handle the routing to the other services behind the scenes.  The other three were the party, player, and equipment services.  Each service had a model, a controller, a service layer, and a repo layer.  Two, the player and equipment, were given DTOs in order to facilitate communication between services with rest template calls.  Standard methods for getting and posting by id were made, as well as methods to return a player with its party or equipment with its player.  The final two methods allow the user to get a list of all members in a party, or all equipment associated with a player. 

## Result and Reflection

The project serves the basic function of what I had intended.  Given more time, I would expand the functionality of these services to allow more useful GET requests using @RequestParams among other additions.

Learning microservices was fun.  I felt I understood the basic concepts easier than I had with some other projects I've worked on.  I have learned that this might be something I want to actively pursue doing in my development career and will be looking more into microservices in the future.  
