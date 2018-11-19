The installation is simple.

### Requirements
- npm
- composer
- php7+

### Installation
```bash
npm i -g vallo-cli

# requires an empty directory
vallo init

# customize the config.php to your needs
nano config.php
```

Internally the `vallo init` command fetches the latest release, extracting it to the current directory and runs `composer install` - that's all.