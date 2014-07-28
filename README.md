composer-foreach
================

`composer-foreach` is a simple replacement for `git submodule foreach` command.
It iterates over all composer packages installed as git repositories and
performs given command.

Aim of this composer-foreach is to ease pushing to multiple repositories at
once, for example when working on application wich heavily uses plugins managed
by Composer.

It works only with git. All other repositories are silently ignored.

Pull requests welcomed.


Examples
--------

~~~~~bash
# Show status of all packages
composer-foreach git status

# Push everything to server
composer-foreach git push

# Make fun of Composer
composer-foreach rm -f composer.json
~~~~~


TODO
----

  - Support basic filtering: by repository type, by package vendor, ...
  - Detect dumb terminal and disable colors.
  - Rewrite this naive prototype (some day).
  - https://github.com/composer/composer/issues/3126


License
-------

Same as Composer's license:

> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is furnished
> to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in all
> copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
> THE SOFTWARE.

