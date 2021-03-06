## Handy things to run
* Normal use:
 * `docker build -t julia-2-js .`
 * `docker run --rm -it -p 5000:5000 julia-2-js`
* Debug work:
 * `docker run --rm -it -p 5000:5000 --entrypoint=/bin/bash julia-2-js`
 * `docker run --rm -it -v ~/work:/work julia-2-js` but with your own path if you want to pass files around (probably need to set entrypoint)
 * Try the node server outside the docker image (conversion calls are unlikely to work): `node ./webserver/index.js`
* Deploying to heroku:
 * `docker tag julia-2-js registry.heroku.com/julia-2-js/web`
 * `docker push registry.heroku.com/julia-2-js/web`
