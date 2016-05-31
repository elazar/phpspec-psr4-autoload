This is an example of using a PSR-4 autoloader with phpspec.

# How it works

In your [Composer PSR-4 autoloader](https://getcomposer.org/doc/04-schema.md#psr-4), make sure the namespace is consistent with the `namespace` and `psr-4_prefix` [settings](http://www.phpspec.net/en/latest/cookbook/configuration.html#psr-4) for your test suite in your `phpspec.yml` file. Review those files in this repository for an example.

# Usage

## Install phpspec

```bash
composer global require phpspec/phpspec
```

Example output:

```
Changed current directory to ~/.composer
Using version ^2.5 for phpspec/phpspec
./composer.json has been updated
Loading composer repositories with package information
Updating dependencies (including require-dev)
Nothing to install or update
Generating autoload files
```

## Generate Composer autoloader

```bash
composer install
```

Example output:

```
Loading composer repositories with package information
Updating dependencies (including require-dev)
Nothing to install or update
Generating autoload files
```

## Generate test

```bash
phpspec describe Acme/Text/Markdown
```

Example output:

```
Specification for Acme\Text\Markdown created in spec/MarkdownSpec.php.
```

## Generate source file

```bash
phpspec run
```

Example output:

```
Acme/Text/Markdown
  10  - it is initializable
      class Acme\Text\Markdown does not exist.

                                      100%                                       1
1 specs
1 example (1 broken)
14ms


  Do you want me to create `Acme\Text\Markdown` for you?
                                                                         [Y/n] y

Class Acme\Text\Markdown created in src/Markdown.php.

                                      100%                                       1
1 specs
1 example (1 passed)
11ms
```
