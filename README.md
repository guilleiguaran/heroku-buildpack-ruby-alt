# Heroku buildpack: Ruby + gs + dep

A buildpack to use Ruby (MRI) on Heroku using [dep](https://github.com/cyx/dep/) for
dependency management. 

## Usage

Just create a Heroku app like this:

    heroku create --buildpack https://github.com/guilleiguaran/heroku-buildpack-ruby-alt

## Customization

This uses the last stable version of Ruby available (2.1.2-p95 right
now), if you want to use another version add a .ruby-version file to 
your application with the desired version, for example:

    2.1.0-preview2

By default rackup is used to start the application, you can add a
Procfile if you want to customize the server used, example:

    web: puma -t 8:12 -w 2 -p $PORT -e $RACK_ENV


## License

Copyright (C) 2013 by Guillermo Iguaran

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
