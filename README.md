# tslint loader for webpack

## Usage

Apply the tslint loader as pre/postLoader in your webpack configuration:

``` javascript
module.exports = {
	module: {
		preLoaders: [
			{
				test: /\.ts$/,				
				loader: "tslint"
			}
		]
	},
  // more options in the optional tslint object
	tslint: {
		configuration: {
            rules: {
                quotemark: [true, "double"]
            }
        },

		// tslint errors are displayed by default as warnings
		// set emitErrors to true to display them as errors
		emitErrors: false,

		// tslint does not interrupt the compilation by default
		// if you want any file with tslint errors to fail
		// set failOnHint to true
		failOnHint: true,		

		// name of your formatter (optional)
		formatter: "yourformatter",

		// path to directory contating formatter (optional)
		formattersDirectory: "node_modules/tslint-loader/formatters/"
	}
}
```
## Installation

``` shell
npm install tslint-loader --save-dev
```

## License

MIT (http://www.opensource.org/licenses/mit-license.php)


