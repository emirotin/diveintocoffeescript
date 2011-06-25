**************************************
1. Installing Node.js and CoffeeScript
**************************************

.. highlight:: bash

First of all, make sure you have your favorite text editor, and you terminal ready.

Node.js
=======

Node.js can be installed on any platform - easier on \*nix, harder on Windows.

See short `official instructions <https://github.com/joyent/node/wiki/Installation>`_, 
and `more detailed from howtonode.org <http://howtonode.org/how-to-install-nodejs>`_.

On Mac OSX with MacPorts you can also do
::

    sudo port install nodejs

Now let's test it::

    $ node --version
    v0.4.8

In your case version number may differ, as Node is constantly developed and updated.

Let's create a test file hello.js:

.. literalinclude:: code/chap1/hello.js
    :language: javascript
    :linenos:  

and run it::

    $ node hello.js
    Hello, World!

This was actually our first Node.js program. Let's explain it:

1\) console.log is a function that outputs given text to the terminal from which the Node program was started,

1') in JS lines of text (strings) are marked with the single (\') or double (\") quotes.

NPM
===

NPM stands for Node Package Manager, and is the interface to the centralized storage of Node.js modules.

If you have `curl`, you can
::

    $ curl http://npmjs.org/install.sh | sh

Read `here <https://github.com/isaacs/npm#readme>`_ if you encounter any problems.

CoffeeScript
============

Having `npm` you can install CoffeeScript as simple as
::

    npm install -g coffee-script

Here `-g` means 'install globally', which is what I prefer. You can install a local copy (somewhere under you home directory) 
by omitting this switch.

You may need root priveledges, like running it as
::

    sudo npm install -g coffee-script
 
Now, let's test it::

    $ coffee --version
    CoffeeScript version 1.1.1

Finally, let rewrite our `hello.js` in CoffeeScript:

.. literalinclude:: code/chap1/hello.coffee
    :language: coffeescript
    :linenos:  

and run it::

    $ coffee hello.coffee
    Hello, World!

This was our first CoffeeScript program. Let's see what changed, and what didn't:

0\) Changed: we are now executing it with `coffee` instead of `node`,

1\) Same: we use the same console.log function, because CoffeeScript only changes language *syntax*,

1') Same: in CoffeeScript strings are also marked with the single (\') or double (\") quotes,

1'') Changed: in CoffeeScript parenthesis are optional for function calls. 
Sometimes it makes the calls much more beautiful and readable (not in this case, though).
