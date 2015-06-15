# grunt-aco2sass

> A grunt plugin for creating .sass variables out of .aco files. Currently supports rgb and hsb(->hsv) colors.

## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install git+https://github.com/iamsisar/grunt-aco2sass.git --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-aco2sass');
```

## The "aco2sass" task

### Overview
In your project's Gruntfile, add a section named `aco2sass` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  aco2sass: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    }
  },
})
```

### Options

#### options.nameOverride
Type: `String`
Default value: `undefined`

Used to override the color names in .aco files. aco2sass appends color numbers automatically: my-color-name-1, my-color-name-2 etc.

#### options.notation
Type: `String`
Default value: `rgb`

If set to `hex`, hex values will be used.


### Usage Examples

```js
grunt.initConfig({
  aco2sass: {
    options: {
      nameOverride: "my-color-name"
    },
    main_palette: {
      files: {
        'dest/my_sass_file.sass': ['my_aco_name.aco', 'path_to_my_acos/*.aco'],
      }
    }
  }
})
```


## Release History
0.0.2
