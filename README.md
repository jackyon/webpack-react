<h1>Webpack base structure with reactjs</h1>
> Containing modern web development tools such as Webpack, React Hot Loader, React Router, Redux, Babel, sass, autoprefixer, BrowserSync, Tinypng...

Directory Layout:
```
├── /app/                       # The source code of the application
│   ├── /actions/            	# Redux action creators
│   ├── /assets/            	# Public css/js/images/fonts
│   ├── /components/            # Components/pages
│   ├── /constants/            	# Constants (action types etc.)
│   ├── /containers/            # Components that provide context (e.g. Redux Provider)
│   ├── /public/            	# Static files which are copied into the /dist/ root folder
│   ├── /reducers/            	# Redux reducers
│   ├── /tmpl/               	# Static content (plain HTML or Markdown)
│   ├── /utils/            		# Generic utilities
│   ├── index.js            	# Application bootstrap and rendering
│
├── /build/                     # The folder for compiled output
├── /dist/                      # The folder for deploy output
├── /node_modules/              # 3rd-party libraries and utilities
├── webpack.config.js           # configuration file for webpack
├── package.json                # The list of 3rd party libraries and utilities
```

<h2>Packages Install</h2>
```
$ npm install
```

<h2>Usage</h2>

Dev:
```
$ npm run dev
```
Browser sync:
```
$ npm run browsersync
```
Deploy:
```
$ npm run deploy
```
Image compress:<br>
<h5>PNG:</h5>
```
$ npm run tinypng
```
> hint: png compress is using tinypng service, make sure you change the above api to your owns. 
> Get api: https://tinypng.com/developers (free 500 images/month. )
> after you get the api, run:
> $ tinypng -k I_KC7xGPxXfZPrEbrc-kXWBetAQ323rz 

<h5>JPEG:</h5>
```
fot now, I'm still using jpegmini, this is the best tools to compress the jpeg images that I discovered so far.
the jpegmini app is quite simple to optimize the photos, just simple drag. But I will consider to integrate this super tool into webpack. Still researching...
```


To do:
<ol>
	<li>Thinking a smart way to deploy the files to remote server without using gulp/grunt.</li>
	<li>More usful plugins will include in...</li>
</ol>



<h2>Hints:</h2>
why not using webpack imagein plugin, cause that plugin doesn't save so much sizes. if you have better solution plz contact me.

By default " npm run tinypng" will replace the original png files, there more useage:
```
tinypng [options] [image.png|*.png]
  -k, --api-key       Set default TinyPNG API key.
  -r, --allow-rewrite Rewrite the original files with compressed data.
  -n, --allow-nonpng  Allow you to compress files without .png extention.
  -p, --postfix       Postfix for compressed files when rewriting disabled.
  -h, --help          This message.
  -v, --version       Show version.
```
you can custom the scripts in package.json file.







