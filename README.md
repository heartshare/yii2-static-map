Yii2 Static Map
===============
Extension for generating static maps (for example for contacts page). Now support google map and openstreet map

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist codru/yii2-static-map "*"
```

or add

```
"codru/yii2-static-map": "*"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
<?= \codru\staticmap\StaticMap::widget(
                                      [
                                          'mapType' => \codru\staticmap\StaticMap::GOOGLE_MAP,
                                          'mapOptions' => [
                                              'center' => '{your coordinates}',
                                              'zoom' => '13',
                                              'size' => '640x100',
                                              'scale' => '2',
                                              'language' => Yii::$app->language,
                                              'markers' => [
                                                   'size' => 'tiny',
                                                   '{your coordinates}',
                                              ],
                                          ],
                                      ]
                                      ); ?>```