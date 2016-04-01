# SublimeText PHP Namespace #

PHP Namespace is a **3 in 1** package to use **PHP Namespaces** with **SublimeText 2 and 3**.

## Installation ##

### With Package Control ###

Look for the package named `PhpNamespace`.

### With Git ###

Move to your SublimeText Packages folder and clone it :

```
git clone https://github.com/gl3n/sublime-php-namespace PhpNamespace
```

If you have **SublimeText 3**, use ``ST3`` branch :

```
git checkout ST3
```

## Features ##

### 1. php_namespace_copy ###

It builds the current file namespace and copies it into the clipboard.

Default shortcut : `alt+c`

> Note: It can be used via **Goto File Overlay**.

### 2. php_namespace_insert_use ###

It builds the `use <...>;` statement of the current file namespace and inserts it into the last active file.

Default shortcut : `alt+u`

> Note: It can be used via **Goto File Overlay**.

### 3. php_namespace_insert_namespace ###

It builds and inserts (or replaces) the `namespace <...>;` statement of the current file.

Default shortcut : `alt+i`

### 4. php_namespace_clean ###

This command scan the current file namespaces and check remove those that are no longer used.

Default shortcut : `alt+r`

### 5. php_namespace_extend ###

This awesome command extends or implements the selected class or interface, all abstract method that does not exist are automaticly implemented and the `use <...>;` statement is inserted.

Default shortcut : `alt+u`

## Settings ##

```
{
    "php_namespace.stop_folders": [
        "src",
        "workspace"
    ]
}
```

The `php_namespace.stop_folders` setting is used for `php_namespace_insert_namespace` command. It defines the folders where the namespace building has to stop.

### PSR-4

> This setting requires the use of the Sublime Text project feature.

In order to have your namespace generated following a PSR-4 convention, add the following entry to your project settings (`Project` > `Edit Project`) :

```
{
    …
    "psr-4":
    {
        "src": "Acme\\"
    }
}
```

The scheme follows the one found in a classical `composer.json`.
