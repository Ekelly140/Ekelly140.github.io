---
layout: post
title:      "Basketball-CLI Gem"
date:       2018-05-25 02:17:39 +0000
permalink:  basketball-cli_gem
---


For my first porfolio project I've chosen to create a gem that can list all of the NBA teams and give you information about any given player on that team. 

The gem works by creating several classes to scrape data on teams and players then reporducing that data in a user friendly format. 

The first class I created was the CLI. The cli(command line interface) is responsible for calling all the methods that will be used in this gem. This is the primary means that users will interact with the application.  

The second class I created was the team class.  The team class was responsible for creating individual team classes that contain a list of players and many  methods. At first these methods were hard coded to have the programing running without breaking, but were later replaced with data from the scrape_team class. The methods in the team class include: Create_from_collection, which takes in an array of teams from team scraper and creates individual teams from it., List_teams which list all the teams in alphabetical order, Get_team, which takes in an input from a user and corrisponds it the appropriate team, Add_player, which adds  a player to a team and list players, which list all the players for a given team.

The third class I created was the team_scraper class. This class was responsible for going to the team section of NBA.com and scraping the team name and team url from each team and creating an array containing each teams data. It then passes this data to the cli so it can be used by the team class to create teams and the player_scraper class to access a list of players.

After creating the the team_scraper class I fixed the hard coding of the team class to load in the information from team scraper.

From there I followed a similar process with the player class and the player scraper class. I hard coded a player class that had several methods such as create_from_collection and get_player.  These methods function similarly to their team counter parts wit hthe addition to displaying additional information about the player.  The player_scraper class however went a layer deeper that its team coutnerpart. In addition to scraping the team page for all of the players names, number and url it went to that players url and grabbed that players birthday, age, and years they have been in the league.

After fixing the hard coding and adding the new methods to the CLI the program was finished and I began cleaing up the code and improving the readiblity.  
