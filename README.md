# Nova Sidebar Icons

Set icons for resources in sidebar.

![screenshot](https://i.imgur.com/mB4nKmY.png)

## Installation

You can install the package in to a Laravel app that uses [Nova](https://nova.laravel.com) via composer:

```bash
composer require anaseqal/nova-sidebar-icons
```

Publish navigation view file:

```bash
php artisan vendor:publish --provider="Anaseqal\NovaSidebarIcons\ToolServiceProvider" --force
```

Register the tool in `NovaServiceProvider`:

```php
use Anaseqal\NovaSidebarIcons\NovaSidebarIcons;
...

public function tools()
    {
        return [
            new NovaSidebarIcons,
            ...
        ];
    }

```

## Usage

set the icon in your nova resource, for example:

```php
    /**
     * The icon of the resource.
     *
     * @var string
     */
    public static $icon = '
        <svg class="sidebar-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path fill="var(--sidebar-icon)" d="M4.06 13a8 8 0 0 0 5.18 6.51A18.5 18.5 0 0 1 8.02 13H4.06zm0-2h3.96a18.5 18.5 0 0 1 1.22-6.51A8 8 0 0 0 4.06 11zm15.88 0a8 8 0 0 0-5.18-6.51A18.5 18.5 0 0 1 15.98 11h3.96zm0 2h-3.96a18.5 18.5 0 0 1-1.22 6.51A8 8 0 0 0 19.94 13zm-9.92 0c.16 3.95 1.23 7 1.98 7s1.82-3.05 1.98-7h-3.96zm0-2h3.96c-.16-3.95-1.23-7-1.98-7s-1.82 3.05-1.98 7zM12 22a10 10 0 1 1 0-20 10 10 0 0 1 0 20z"
            />
        </svg>
    ';
```

## License

The MIT License (MIT). Please see [License File](LICENSE) for more information.

