#base64image

image base64 encoder

## Install

**Node.js 4 or higher**

    $ npm install @huang.xinghui/base64image --save

## Usage

    // Stream Usage
    var base64image = require('@huang.xinghui/base64image')
    // imagePath can be a url path, such as 'http://example.com/assets/img.png'
    // or a absolute path, such as 'C:/foo/img.png'
    // or a releative path, such as './img.png'
    base64image.stream(imagePath).pipe(process.stdout)

    // Common Usage
    var base64image = require('@huang.xinghui/base64image')
    base64image(imagePath).then(function(data) {
      console.log(data)
    })

## API

- base64image(imagePath)
    base64 encode image, return `Promise`
- base64image.stream(imagePath)
    base64 encode image, return `Stream`
