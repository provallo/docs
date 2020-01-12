# Get Started - Build your own Plugin

Plugins are generally stored in the `ext/`-Directory of your installation. The simplest plugin you can
imagine contains a `plugin.json` and a `Bootstrap.php`

The plugin.json contains meta information about the plugin. The basic structure looks like this:

```json
{
  "name": "<technical plugin name>",
  "label": "<plugin name, must equal the directory name>",
  "description": "<the description of the plugin, what it does>",
  "author": "<your name>",
  "website": "<your website>",
  "email": "<your email>",
  "version": "<current version>",
  "changelog": {
    "1.0.0": [
      "Initial release"
    ]
  },
  "requires": {
    "Backend": "1.1.3"
  }
}
```

A minimalistic Bootstrap.php

```php
<?php

namespace ProVallo\Plugins\YourPluginName;

use ProVallo\Core;

class Bootstrap extends \ProVallo\Components\Plugin\Bootstrap
{
    
    public function execute()
    {
        // your plugin logic here
    }

}
```

When you look at the `ProVallo\Components\Plugin\Bootstrap` class you'll find additional methods such as `install`, 
`update` and `uninstall`. These are lifecycle callbacks of the plugin (when a plugin gets installed, updated or removed)

