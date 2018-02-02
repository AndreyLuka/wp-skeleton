# WordPress Skeleton

WordPress skeleton with Composer, readiness for VCS and improved project structure.  

## Requirements

* [PHP](https://php.net/) >= 5.6
* [Composer](https://getcomposer.org/)

## Installation

1. Go to a new project directory and type:  
`git clone https://github.com/AndreyLuka/wp-skeleton.git .`
2. Copy `/public/wp-config.dist.php` to `/public/wp-config.php` and edit variables (database connection, etc).
3. Run `composer install`
4. Visit site URL to run WordPress installation.
5. Add theme(s)/plugin(s) (read below).

## Themes installation

Install themes using Composer:  
`composer require wpackagist-theme/<theme-name>`

By default, all themes are ignored by git. If you need to keep theme in repository (custom theme, child theme, etc) add this line to .gitignore:  
`!/wp-content/themes/<theme-name>/`

## Plugins installation

Install plugins using Composer:  
`composer require wpackagist-plugin/<plugin-name>`

By default, all plugins are ignored by git. If you need to keep plugin in repository (custom plugin, etc) add this line to .gitignore:  
`!/wp-content/plugins/<plugin-name>/`

## Project structure

```
<project-name>/            # Project directory
├── public/                # Document root
│   ├── wp/                # WP core
│   ├── wp-content/        # WP content
│   ├── .htaccess          # Main .htaccess
│   ├── index.php          # WP index.php
│   ├── wp-config.dist.php # WP config dist
│   └── wp-config.php      # WP config
├── vendor/                # Composer packages
├── .editorconfig          # editorconfig.org
├── .gitignore             #
├── .htaccess              # .htaccess for servers where document root cannot be changed
├── composer.json          # Composer dependencies
├── composer.lock          # Composer lock file
├── LICENSE.md             #
└── README.md              #
```
