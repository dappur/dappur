# dApp

This is the command line interface for the [Dappur PHP Framework](https://github.com/dappur/framework)

## Pre-Requisites
[Composer](https://getcomposer.org/) - Dependency manager is required in order to use the Dappur PHP Framework.  [Installation Instructions](https://getcomposer.org/doc/00-intro.md)

[Phinx](https://phinx.org/) - Phinx is required in order to utilize the database migrations.  It is recommended that you install Phinx globally via composer by running:

    $ composer global require robmorgan/phinx

## Installation

    $ composer global require dappur/dapp

## Usage
### `new`
This command creates a new Dappur application in the specified folder using the composer `create-project` command.
- **name** - The folder name for your new appliciation.
```
$ dapp new name
```

### `controller`
This command generated a new controller class in `app/src/Controller` as well as having the controller automatically added to the container dependencies with an entry in `app/src/bootstrap/controllers.php`
- **name** - The name of your controller class in `PascalCase` format.  This command also supports generating nested class names, i.e. `NewController\SubController`.
```
$ dapp controller name
```

### `app`
This command generated a new App class template in `app/src/App` using the class name that you specify.
- **name** - The name of your class in `PascalCase` format.  This command also supports generating nested class names, i.e. `NewController\SubController`.
```
$ dapp app name
```

### `middleware`
This command generated a new App class template in `app/src/Middleware` using the class name that you specify.
- **name** - The name of your class in `PascalCase` format.  This command also supports generating nested class names, i.e. `MyMiddleware\SubMiddleware`.
```
$ dapp middleware name
```

### `twigex`
This command generated a new App class template in `app/src/TwigExtensions` using the class name that you specify.
- **name** - The name of your class in `PascalCase` format.  This command also supports generating nested class names, i.e. `MainExtension\SubExtension`.
```
$ dapp twigex name
```

### `server`
This command launches an instance of PHP's built-in web server, `php -S` defaulted to port 8181.
- **port (Optional)** - Port to run the web server on.  Default is 8181.
```
$ dapp server port
```