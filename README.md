#SyntaxHighlightBundle

The package encapsulates into Symfony/composer bundle following Syntax Highlighter

    SyntaxHighlighter 
    version 3.0.83 (July 02 2010)
    http://alexgorbatchev.com/SyntaxHighlighter
    JavaScript code syntax highlighter.
    Copyright 2004-2010 Alex Gorbatchev.

### **INSTALLATION**:

First add the dependency to your `composer.json` file:

    "require": {
        ...
        "adiog/syntax-highlight-bundle": "dev-master"
    },

Then install the bundle with the command:

    php composer.phar update

Enable the bundle in your application kernel:

``` php
<?php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Adiog\SyntaxHighlightBundle\SyntaxHighlightBundle(),
    );
}
```

Now install assets:

    php bin/console assets:install [--symlink]
