#SyntaxHighlightBundle

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

    php app/console assets:install [--symlink]
