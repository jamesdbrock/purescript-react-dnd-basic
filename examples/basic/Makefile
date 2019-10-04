all: node_modules
	$(shell npm bin)/purs compile src/*.purs '../../src/**/*.purs' '../../bower_components/purescript-*/src/**/*.purs'
	$(shell npm bin)/purs bundle --module Basic output/*/*.js > output/bundle.js
	echo 'module.exports = PS.Basic;' >> output/bundle.js
	$(shell npm bin)/browserify output/bundle.js index.js -o html/index.js

node_modules:
	npm install
