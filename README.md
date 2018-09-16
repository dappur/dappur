# dApp

This is the command line interface for the [Dappur PHP Framework](https://github.com/dappur/framework)

## Pre-Requisites
[Composer](https://getcomposer.org/) - Dependency manager is required in order to use the Dappur PHP Framework.  [Installation Instructions](https://getcomposer.org/doc/00-intro.md)

[Phinx](https://phinx.org/) - Phinx is required in order to utilize the database migrations.  It is recommended that you install Phinx globally via composer by running:

    $ composer global require robmorgan/phinx

## Installation

    $ composer global require dappur/dapp

## Usage
### Framework Commands
#### `new`
This command creates a new Dappur application in the specified folder using the composer `create-project` command.
- **Name** - The folder name for your new appliciation.
```
$ dapp new {Name}
```

#### `controller`
This command generated a new controller class in `app/src/Controller` as well as having the controller automatically added to the container dependencies with an entry in `app/src/bootstrap/controllers.php`
- **Name** - The name of your controller class in `PascalCase` format.  This command also supports generating nested class names, i.e. `NewController\SubController`.
```
$ dapp controller {Name}
```

#### `app`
This command generated a new App class template in `app/src/App` using the class name that you specify.
- **Name** - The name of your class in `PascalCase` format.  This command also supports generating nested class names, i.e. `NewController\SubController`.
```
$ dapp app {Name}
```

#### `middleware`
This command generated a new App class template in `app/src/Middleware` using the class name that you specify.
- **Name** - The name of your class in `PascalCase` format.  This command also supports generating nested class names, i.e. `MyMiddleware\SubMiddleware`.
```
$ dapp middleware {Name}
```

#### `twigex`
This command generated a new App class template in `app/src/TwigExtensions` using the class name that you specify.
- **Name** - The name of your class in `PascalCase` format.  This command also supports generating nested class names, i.e. `MainExtension\SubExtension`.
```
$ dapp twigex {Name}
```

#### `server`
This command launches an instance of PHP's built-in web server, `php -S` defaulted to port 8181.
- **Port (Optional)** - Port to run the web server on.  Default is 8181.
```
$ dapp server {Port}
```

### Database Commands
#### `mc`
This command created a new migration using the Phinx `phinx create` command.
- **Name** - The name of your migration in `PascalCase` format.
```
$ dapp mc {Name}
```

#### `migrate`
This command created a new migration using the Phinx `phinx migrate` command.
- **Environment (Optional)** - Target the migration on a specific environment.
- **Target (Optional)** - Target a specific migration.
```
$ dapp migrate -e {Environment} -t {Target}
```

#### `rollback`
This command created a new migration using the Phinx `phinx rollback` command.
- **Environment (Optional)** - Target the migration on a specific environment.
- **Target (Optional)** - Target a specific migration.
```
$ dapp rollback -e {Environment} -t {Target}
```

#### `breakpoint`
This command created a new migration using the Phinx `phinx breakpoint` command.
- **Environment (Optional)** - Target the breakpoint on a specific environment.
- **Target (Optional)** - Target the breakpoint on a specific migration.
- **Remove All (Optional)** - Remove all breakpoints.
```
$ dapp breakpoint -e {Environment} -t {Target} -r
```