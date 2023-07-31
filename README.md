# AllNewsy News Aggregator

 ![Watch the video](https://i.ytimg.com/vi/BNflNL40T_M/hq720.jpg?sqp=-oaymwEcCOgCEMoBSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLCdqjE42x_2rjSEe7BlGJycSffalw)

## Background

This repo is the home of the News Aggregator task for Innoscripta AG. The application is a dockerized Laravel 10 + React.Js (Typescript) application using a mysql database.

The website handles the scraping of online APIs from the ones provided in the challenge/task description. Namely the following:

 - NewsAPI
 - The Guardian
 - The New York Times
 
 The scraping process is done in the background at an hourly interval through a dedicated job that's autoamtically added when running docker compose through the Laravel backend's entrypoint.

## Getting Started

To install and run the projects, make sure you have the following installed:

 - Git
 - Docker Compose
 - Docker Engine (I'm using version 20.x)

### Installation

 1. Clone the project
 ```bash
  $ git clone https://github.com/dystopian228/innoscripta-allnewsy-task.git
  $ cd innoscripta-allnewsy-task
  ```
  
 2. Fetch and pull submodules
 ```bash
  $ git submodule init
  $ git submodule update
  ```
 4. Update environment variables: In the docker-compose file, update the environment values you need to change depending on your own. (Especially for the APIs variables)
 5. Run docker-compose
 ```bash
  $ docker-compose up -d
 ```

### Using the project

The frontend is exposed on port 3000:

`http://localhost:3000`

While the backend API is on port 8080:

`http://localhost:8080`
