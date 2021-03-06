grunt-image-autoresize
=============

Automatically resizes images if the width or height is greater than a certain dimension. Keeps the aspect ratio.

For example, let's say you set the maximum dimension setting to 1000px. If an image is 2000x1000px, it gets resizes it to 1000x500px. If the image is 1000x2000px, it becomes 500x1000px.

The default max dimension is 800 pixels and can be changed. With the default option, the 2000x1000px image would be resized to 800x400px.

This uses ImageMagick, so it requires ImageMagick to be installed. Thus this only supports images supported by ImageMagick.

## Config
```javascript
grunt.initConfig({
    image_autoresize: {
        target_name_here: {
            maxdimension: 1000, // optional
            files: [{
              cwd: 'current working directory here',
              src: '**/*.{png,jpg}',
              dest: 'some output directory here'
            }]
        }
    }
})
```

The `files` value is an array of objects, the specifics of which can be read in [Grunt globbing pattern docs](https://gruntjs.com/configuring-tasks#globbing-patterns).

## Example configuration
```javascript
grunt.initConfig({
    image_autoresize: {
        target_name_here: {
            files: [{
              cwd: 'static/img',
              src: '**/*.{png,jpg}',
              dest: 'public/img'
            }]
        }
    }
})
```

