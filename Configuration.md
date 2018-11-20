The default configuration is located at `src/Config/Default.php`. It can be extended in `config.php` returning a simple array containing the data that should be replaced by `array_replace_recursive` (see `src/Config.php`)

```php
[
    'config'   => [
        // Controller modules (more information later)
        'modules'   => [],
        // The view/themes configuration (paths are relative to app.path)
        'view'      => [
            'theme_path' => 'themes/',
            'cache_path' => 'cache/twig/'
        ],
        // The default database configuration (currently only MySQL is supported)
        'database'  => [
            'host' => '%database.host%',
            'shem' => '%database.shem%',
            'user' => '%database.user%',
            'pass' => '%database.pass%'
        ],
        // Basic app configuration
        'app'       => [
            // The absolute root path
            'path'       => realpath(__DIR__ . '/../..') . '/',
            // The cache path (relative to app.path)
            'cache_path' => 'cache/'
        ],
        // The plugins configuration
        'plugin'    => [
            // The plugin path is relative to the app.path
            'path' => 'ext/'
        ],
        // The http-cache configuration
        'httpCache' => [
            'enabled' => true
        ],
        // The cookie configuration
        'cookie'    => [
            'enabled' => true,
            'config'  => [
                'name'        => 'provallo',
                'lifetime'    => '1 year',
                'autorefresh' => true
            ]
        ],
        // The debug mode enables better exceptions
        'debug' => true
    ],
    // Slim framework related settings
    'settings' => [
        'displayErrorDetails' => true
    ]
];
```