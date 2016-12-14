YII 2 ADMIN LTE CRUD
==========================


## Установка CRUD шаблона

Код для интеграции adminlte шаблона к CRUD в Gii.
Нужно выполнить:

    composer require ceyhunism/yii-adminlte-crud-template

или добавить в composer.json в "required"

    "ceyhunism/yii-adminlte-crud-template": "dev-master"

----
Альтернативный способ установки:
    Скопировать весь проект ceyhunism/yii-adminlte-crud-template в папку @vendor

## Настройка GII шаблона

В конфигурационном файле /config/main.php нужно добавить:

```````
$config['modules']['gii'] = [
        'class' => 'yii\gii\Module',
          'generators' => [ 
            'crud' => [
                'class' => 'yii\gii\generators\crud\Generator', // generator class
                'templates' => [ 
                    'custom' => '@vendor/ceyhunism/yii-adminlte-crud-template',
                ]
            ]
        ],
    ];
```````


После этого при использовании CRUD в Gii в разделе "Code Template" необходимо выбрать соответствующий шаблон.
