# ruslanskorb.com

The website [ruslanskorb.com](http://ruslanskorb.com)

### How to start server

```sh
$ npm start
```

### How to develop

```sh
$ gulp
```

### How to deploy

```sh
heroku git:remote -a ruslanskorb
git push heroku master
```

### Gulp tasks

- `gulp`: Builds and watches for changed files
- `gulp build`: Compiles and builds the generated files
- `gulp watch`: Watches files
- `gulp coffee`: Lints coffeescript and browserifies client coffeescript
- `gulp stylus`: Compiles stylus
- `gulp image`: Minifies images

### Built with

- :coffee: Coffeescript
- :cloud: Express
- :lipstick: Stylus
- :gem: Jade
- :tropical_fish: Gulp
