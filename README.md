# CircleCI & Node.js demo

![](app.gif)

# Setting Up A Demo

The "demo" is designed to provide a simple proof of concept for a typical use-case on CircleCI, demonstrating CI/CD in practice as well as several product features (e.g. Workflows, Contexts, etc).

NOTE: reset.sh assumes BSD (mac) `sed`

## Prereqs

1. Account on Heroku, an application running on heroku, and a Heroku API key
1. Github account and Github API key
1. An account on CircleCI associated with your Github account and a CircleCI API key

## Getting started

1. Makefiles are your friend. Run `make init` to create your secrets file and fill in the appropriate values, i.e. API keys, etc.
1. If you DO NOT have a heroku application setup, you can create one by running `make heroku`; a heroku application is a logical grouping of resources, e.g. a docker container with unique configuration settings, a CNAME pointing to the application, etc. Meaning...creating a heroku "application" doesn't entail the application we're building on CircleCI, it just provisions the infrastructure.
1. ONCE you have a heroku application setup and the correct values input in the secrets file, run `make` (no args) to provision the demo. Run the demo. Close some deals. Motivate.

## CircleCI features
1. Executors
2. Workflows
3. (Dependency) Caching
4. Contexts
5. Resource Classes
6. Continuous Deployment via Heroku
7. 1st class Docker support, DLC, etc

## How the Demo actually works

The demo consists of building, testing, and subsequently deploying a containerized node js application to Heroku.

The demo flow consists of...