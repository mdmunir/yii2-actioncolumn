Action Colum
============
Action column dg button sesuai role

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist mdmunir/yii2-actioncolumn "dev-master"
```

or add

```
"mdmunir/yii2-actioncolumn": "dev-master"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
\Yii::$container->set('yii\grid\ActionColumn', [
    'class' => 'mdmunir\grid\ActionColumn',
    'visibleCallback' => function($name) {
        return \Yii::$app->user->can(\Yii::$app->controller->id . '/' . $name);
    },
]);
```