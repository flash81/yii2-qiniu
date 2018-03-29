文件上传到七牛
=================================
* @author flash20 <2684498887@qq.com>
* @version 1.0

file upload for qiniu

最近会调整版本

```json
{
  "require": {
    "flash20/yii2-qiniu": "*"
  }
}
```
```php
composer install
```

Usage
-----

```main.php
<?php
        'qiniu'=> [
            'class' => 'flash20\qiniu\Qiniu',
            'accessKey' => 'xxx',
            'secretKey' => 'xxx',
            'domain' => 'http://xxx',
            'bucket' => 'xxx',
        ],
```
```code
Yii::$app->qiniu->uploadFile($file,time());
```
