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
        "alten/syntax-highlight-bundle": "dev-master"
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
        new Alten\SyntaxHighlightBundle\AltenSyntaxHighlightBundle(),
    );
}
```

Now install assets:

    php bin/console assets:install [--symlink]

### **USAGE**

Add the following lines to your base twig file:
``` html
<script type="text/javascript" src="{{ asset('bundles/adiogsyntaxhighlight/js/scripts/shCore.js') }}"></script>
<script type="text/javascript" src="{{ asset('bundles/adiogsyntaxhighlight/js/scripts/shAutoloader.js') }}"></script>
<script type="text/javascript" src="{{ asset('bundles/adiogsyntaxhighlight/js/scripts/shBrushJScript.js') }}"></script>
	<script type="text/javascript" src="{{ asset('bundles/adiogsyntaxhighlight/js/scripts/shBrushCpp.js') }}"></script>
	<link type="text/css" rel="stylesheet" href="{{ asset('bundles/adiogsyntaxhighlight/css/styles/shCoreDefault.css') }}"/>
	<script type="text/javascript">SyntaxHighlighter.all();</script>
```

And in a WYSYWIG editor you may switch to raw mode and use a &lt;pre class="brush: cpp"&gt; tag:
``` html
<pre class="brush: cpp">
#include <iostream>

int main() {
	std::cout << "Hello world!" << std::endl;
	return 0;
}
</pre>
```

