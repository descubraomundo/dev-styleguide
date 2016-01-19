# Dev Style Guide V1.0

## Coding Style

All Projects follows the [PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) coding standard and the [PSR-4](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md) autoloading standard.

### Namespace
#### Internal
##### Apps
In this case the vendor namespace should be the app name;
##### Services
In this case the vendor namespace it should be `DMI\Services\`.
#### Open Source
If it is a open source project, it should should have the vendor package as `Descubraomundo`.

### Class Methods and Properties

The class methods and properties must be in `camelCase` like:
```php
<?php

Class Invoice
{
    protected $publicNotes = '';

    public function getPublicNotes()
    {
        return $this->publicNotes;
    }
}

```

### Variable Names

All variables must be in `snake_case` style like:
```php
<?php

$email_marketing = 'example@test.com';
```

## DocBlocks

DocBlocks are divided into the following three parts. Each of these parts is optional, except that a Description may not exist without a Summary.

### Example
A DocBlock looks like this:
```php
<?php
 /**
  * A summary informing the user what the associated element does.
  *
  * A *description*, that can span multiple lines, to go _in-depth_ into the details of this element
  * and to provide some background information or textual references.
  *
  * @param string $myArgument With a *description* of this argument, these may also
  *    span multiple lines.
  *
  * @return void
  */
  function myFunction($myArgument)
  {
  }
```

### Laravel Projects
#### Views
As we do not work with ActiveRecord(eloquent), it is fine to always pass an **Object** to the views and work with our entities. 

#### I18N
For all the lang files, the keys should always be in `english` and in `snake_case` style like:
```php
<?php
    return [
        'hello_world' => 'Hello World!'
    ];
```


## Branch Contribution

All bug fixes should be sent to the latest stable branch. Bug fixes should never be sent to the master branch unless they fix features that exist only in the upcoming release.

Minor features that are fully backwards compatible with the current Project release may be sent to the latest stable branch.

Major new features should always be sent to the master branch, which contains the upcoming Project release.

If you are unsure if your feature qualifies as a major or minor, please ask Team Members.

Its recommended to use git extensions like [gitflow](https://github.com/nvie/gitflow) to provide repository operations for Vincent Driessen's [branching model](http://nvie.com/posts/a-successful-git-branching-model/).
