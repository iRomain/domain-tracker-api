About
=====

I use this api to track my domains across various registrars.

It is licensed under [MIT](https://en.wikipedia.org/wiki/MIT_License), so feel free to use it for any project and of course please feel free to raise issues and contribute through pull requests. 

[Demo](https://domain-tracker-api.herokuapp.com/documentation) (hosted on heroku free plan - available 18h/day)


Features
========

 - Server: [NodeJS](https://nodejs.org)
 - Linting: [Standard](http://standardjs.com)
 - API:
   - Framework: [Hapi](http://hapijs.com)
   - Testing: [Lab](https://github.com/hapijs/lab), [Code](https://github.com/hapijs/code)
   - Validation: [Joi](https://github.com/hapijs/joi)
   - Documentation: [Swagger](http://swagger.io)


Installation
============

Clone this repository to your development machine:

`git clone https://github.com/iRomain/domain-tracker-api.git`

Enter the newly created directory:

`cd domain-tracker-api`

Install NPM dependencies:

`npm install`


Dev
===
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](http://standardjs.com/)

Run `npm run dev-start`, it will automatically test, lint and start your API, watching any modification and re-linting/starting with nodemon.

NPM sets the environment variable `NODE_ENV=dev`

> Use [TDD](https://en.wikipedia.org/wiki/Test-driven_development):

> 1. Write a test in `./test/`
> 2. Add your endpoint in `./lib/api.js`
> 3. Run `npm run dev-start`

You can see your API on [http://localhost:3000](http://localhost:3000) and see its documentation on [http://localhost:3000/documentation](http://localhost:3000/documentation)


Test
====

Travis CI [![Build Status](https://api.travis-ci.org/iRomain/domain-tracker-api.svg)](https://travis-ci.org/iRomain/domain-tracker-api)
---------

This API is compatible with [Travis](https://travis-ci.org).

It sets the environment variable `NODE_ENV=test`

> Add this repo (which you most likely forked already):

> 1. [Sync Travis with your Github account](https://travis-ci.org/profile) and add this repo
> 2. Push your repo (if you didn't change/remove the [`deploy`](.travis.yml#L7) part, it will fail at deployment)

Code Climate [![Code Climate](https://codeclimate.com/github/iRomain/domain-tracker-api/badges/gpa.svg)](https://codeclimate.com/github/iRomain/domain-tracker-api) [![Test Coverage](https://codeclimate.com/github/iRomain/domain-tracker-api/badges/coverage.svg)](https://codeclimate.com/github/iRomain/domain-tracker-api/coverage)
------------

This API is compatible with [Code Climate](https://codeclimate.com) through the [Travis/Code Climate integration](http://docs.travis-ci.com/user/code-climate/)

> 1. Add this repo to Code Climate and get the repo token
> 2. Edit the `addons.code_climate.repo_token` in [.travis.yml](.travis.yml)
> Tip: Use [Travis to encrypt](http://docs.travis-ci.com/user/encryption-keys/) your token with `travis encrypt <token> --add addons.code_climate.repo_token`

This API is also compatible with Codacy [![Codacy Badge](https://api.codacy.com/project/badge/5e7e5bcce27744baad9248c94e3e98c9)](https://www.codacy.com/app/iRomain/domain-tracker-api)


Prod
====

Heroku hosting [![Deployment Status](http://heroku-badge.herokuapp.com/?app=domain-tracker-api&style=flat&root=documentation)](https://domain-tracker-api.herokuapp.com/documentation)
--------------

This API is compatible with [Heroku](http://keroku.com) through the [Travis/Heroku integration](http://docs.travis-ci.com/user/deployment/heroku/).

> [Create a new app](https://dashboard.heroku.com/new) on Heroku:

> Change the Deploy configuration in [.travis.yml](.travis.yml):

> 1. Change your `deploy.app` name
> 2. Change your `deploy.api_key`
> Tip: Use [Travis to encrypt](http://docs.travis-ci.com/user/encryption-keys/) your api key with `travis encrypt <api key>`

> Push to GitHub:

> 1. Watch the build in Travis
> 2. Watch the deployment in Heroku
> 3. Your API is now available on `https://<app name>.herokuapp.com/documentation`

Docker image
--------------
A [Docker image](https://hub.docker.com/r/iromain/domain-tracker-api/) is automatically built by using the [Travis/Docker integration](http://docs.travis-ci.com/user/docker/). It could be setup with docker hub [automated build](https://hub.docker.com/add/automated-build) functionality but I prefer how everything can be configured in .travis.yml close to the code.

> Change the Docker image build configuration in [.travis.yml](.travis.yml):

> 1. Change your image repo in `before_install` for both the build and push commands
> 2. Change your [encrypted](http://docs.travis-ci.com/user/encryption-keys/) docker email, username, password in `env`


New Relic monitoring
--------------------

This API is compatible with [New Relic](http://newrelic.com) through the [Heroku/New Relic integration](https://docs.newrelic.com/docs/agents/nodejs-agent/hosting-services/nodejs-agent-heroku)

> 1. [Add the New Relic element](https://elements.heroku.com/addons/newrelic) to your app
> 2. Edit the `app_name` in [newrelic.js](newrelic.js) with your heroku app name (recommended but could be any name)
> 3. Edit the `logging.level` in [newrelic.js](newrelic.js) to suit [your desired logging level](https://github.com/trentm/node-bunyan#levels)

----------

*Original credits to: [iRomain/api-bootstrap](https://github.com/iRomain/api-bootstrap)*
