# iteclab Web creator | A Web creator

- [iteclab Web creator | A Web creator](#iteclab-web-creator--a-web-creator)
	- [About](#about)
	- [Requirements](#requirements)
	- [Installation](#installation)
	- [Routes](#routes)
	- [Usage](#usage)
	- [Folders](#folders)

## About

Do you want your clients to be able to install a Laravel project just like they do with WordPress or any other CMS?
This Laravel package allows users who don't use Composer, SSH etc to install your application just by following the setup wizard.
The current features are :

- Check For Server Requirements.
- Check For Folders Permissions.
- Ability to set database information.
	- .env text editor
	- .env form wizard
- Migrate The Database.
- Seed The Tables.

## Requirements

* [Laravel 8.0+](https://laravel.com/docs/installation)

## Installation

1. From your projects root folder in terminal run:

```bash
    composer require iteclab/itec-creator
```

2. Register the package

Register the package with laravel in `config/app.php` under `providers` with the following:

```php
	'providers' => [
	    iteclab\itecCreator\Providers\itecCreatorServiceProvider::class,
	];
```

3. Publish the packages views, config file, assets, and language files by running the following from your projects root folder:

```bash
    php artisan vendor:publish --provider="iteclab\itecCreator\Providers\itecCreatorServiceProvider"
```

## Routes

* `/install`

## Usage

* **Install Routes Notes**
	* In order to install your application, go to the `/install` route and follow the instructions.
	* Once the installation has ran the empty file `installed` will be placed into the `/storage` directory. If this file is present the route `/install` will redirect to homepage.

## Folders

|Folder|Folder Information|
|:------------|:------------|
|`public/itecfiles`|This folder contains all the asset files, this file is responsible for the styling of your creator, you can overide the default stylesheet `style.css` and add your own.|
|`resources/views/iteclab/creator`|This folder contains the HTML code for your creator, it is 100% customizable, give it a look and see how nice/clean it is.|


