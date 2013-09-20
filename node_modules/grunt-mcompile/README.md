grunt-mcompile
==============

>   Plugin to compile mustache templates as static html

Getting Started This plugin requires Grunt `~0.4.1`
---------------------------------------------------

If you haven't used [Grunt](<http://gruntjs.com/>) before, be sure to check out
the [Getting Started](<http://gruntjs.com/getting-started>) guide, as it
explains how to create a [Gruntfile](<http://gruntjs.com/sample-gruntfile>) as
well as install and use Grunt plugins. Once you're familiar with that process,
you may install this plugin with this command:

```
shell npm install grunt-mcompile --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with
this line of JavaScript:

```
js grunt.loadNpmTasks('grunt-mcompile');
```

The "mcompile" task
-------------------

### Overview In your project's Gruntfile, add a section named `mcompile` to the data object passed into `grunt.initConfig()`.

```
js grunt.initConfig({
	mcompile: {
		options: {   // Task-specific options go here. },
		your_target: {   // Target-specific file lists and/or options go here. },
	},
})
```

### Options

#### options.templateRoot Type: `String` Default value: `''`

A string value that is used to do has the root location of your mustache
template files.

#### options.dataRoot Type: `String` Default value: `''`

A string value that is used to do has the root location of your mustache
data files.

### Usage Examples

#### Default Options

```
js grunt.initConfig({
	mcompile: {
		options: {},
		files: {
			'dest/': [src/*.html'],
		},
	},
})
```

#### Custom Options

```
js grunt.initConfig({
	mcompile: {
		options: {
			templateRoot: '_data/templates/',
			dataRoot: '_data/json/',
		},
		files: {
			'dest/' : ['src/*.html'],
		},
	},
})
```

Usage
-----

To use the task simply add the data attributes in your source html as follows.

```
<div data-mustacheTemplate="_data/test.mustache" data-mustacheData="_data/test.json">No JS data</div>
```

The element will be replaced with the mustache template.



Contributing In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](<http://gruntjs.com/>).

Release History _(Nothing yet)_
-------------------------------
