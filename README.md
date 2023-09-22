### Hi there 👋
```php
<?php

declare(strict_types=1);

namespace Haian;

final class MyProfile implements UserProfile
{
    public function __construct(
        public readonly int $id = 99519781,
        public readonly string $name = 'Haian Ibrahim',
        public readonly string $username = 'hki98',
        public readonly int $age = 25,
    ) {
    }

    public function getSkills(): array
    {
        return [
            \Language\Php::class => ['versions' => '^4 | ^5 | ^7 | ^8'],
            \Language\Python::class => ['versions' => '^3'],
            \Language\Javascript::class => ['versions' => 'ES3 | ES5 | ES6 | ES7 | ES8 | ES9 | ES 10 | ES11'],
            \Language\Typescript::class => ['versions' => '^4'],
            \Language\Html::class => ['versions' => '^4 | ^5 | dev-xhtml | dev-wml'],
            \Language\Css::class => ['versions' => '^2 | ^3'],
            \Language\Scss::class => ['versions' => '*'],
            \Language\Java::class => ['versions' => '5 - 11'],
            \Language\Bash::class => ['versions' => '^4 | ^5'],
            \Language\Xml::class => ['versions' => '*'],
            \Language\Json::class => ['versions' => '*'],

            \Framework\Backend\Php\Symfony::class => ['versions' => '^3 | ^4 | ^5 | ^6'],
            \Framework\Backend\Php\Yii::class => ['versions' => '~1.1 | ~2.0'],
            \Framework\Frontend\Javascript\React::class => ['versions' => '^16.13 | ^17'],
            \Framework\Fullstack\NextJS::class => ['versions' => '^10.2'],
            \Framework\Fullstack\Django::class => ['versions' => '^4.2.5'],

            \Tools\Webpack::class => ['versions' => '^4 | ^5'],
            \Tools\Gulp::class => ['versions' => '^3.9 | ^4.0'],
            \Tools\Deptrac::class => ['versions' => '*'],
            \Tools\PhpCsFixer::class => ['versions' => '*'],
            \Tools\Infection::class => ['versions' => '*'],
            \Tools\Docker::class => ['versions' => '*'],
            \Tools\DockerCompose::class => ['versions' => '^1 | ^2'],

            \Database\MySQL::class => ['versions' => '~5.1 | ~5.5 | ~5.7 | ^8.0'],
            \Database\PostgreSQL::class => ['versions' => '^12 | ^14'],
            \Database\SQLite::class => ['versions' => '^3.8'],
            \Database\MongoDB::class => ['versions' => '^2.2 | ^3.0 | ^4.0'],

            \Platform\Android::class => ['versions' => '>= 2.1'],
        ];
    }

    public function __toString(): string
    {
        return $this->username;
    }
}
```
