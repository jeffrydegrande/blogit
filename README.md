# Blogit (beta)

Blogit is a flexible blogging solution for Rails apps. It:

* Is Rack based;
* Is a complete MVC solution based on Rails engines;
* Aims to work right out of the box but remain fully customisable.

## Installation

Add this to your Gemfile

``` ruby
gem "blogit"
```

...and run `bundle install` to install the gem.

Next, run:

``` bash
# add an initializer to config/initializers with all of the configuration options
$ rails g blogit:install
# This will add the necessary migrations to your app's db/migrate directory
rake blogit:install:migrations
# This will run any pending migrations
rake db:migrate
``` 
then add the following to your routes.rb file:

``` bash
# config/routes.rb
mount Blogit::Engine => "/blog"
```

... and finally, declare which of your models acts as blogger in your app (usually User).

``` ruby
class User
  
  blogs

end
```  

## Configuration

Running `rails g blogit:install` will add an initializer file named blogit.rb. In here
you can set various configuration options. Please [read the documentation](http://rubydoc.info/gems/blogit/Blogit/Configuration) for a full list of the options available.

## At no extra cost...

we'll also throw in:

* An XML Sitemap located at `/blog/posts.xml`
* An RSS feed located at `/blog/posts.rss`
* Page Caching and Sweeping

## Issues

If you discover a problem with Blogit, please let us know about it. 

**Remember** to search the [issues list](https://github.com/KatanaCode/blogit/issues) first in case your issue has already been raised
by another Githuber

## Documentation

Full documentation is available here: http://rubydoc.info/gems/blogit

## Contributing

You're welcome to contribute to Blogit. Please consult the [contribution guidelines](https://github.com/KatanaCode/blogit/wiki/Contributing) for more info.

## Legal Stuff

Copyright 2011 [Katana Code Ltd.](http://katanacode.com)

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Credits

Developed by [katana:code](http://katanacode.com)

## About katana:code

katana:code are [Ruby on Rails Developers Based in Edinburgh, Scotland](http://katanacode.com/ "katana:code").