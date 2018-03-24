文件上传到七牛
=================================
* @author flash20 <2684498887@qq.com>
* @version 1.0
test
file upload for qiniu


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

```php
<?php
$ak = 'sss';
$sk = 'sss';
$domain = 'http://demo.domain.com/';
$bucket = 'demo';
$zone = 'south_china';
use flash20\qiniu\Qiniu;
$qiniu = new Qiniu($ak, $sk,$domain, $bucket,$zone);
$key = time();
$key .= strtolower(strrchr($_FILES['name'], '.'));

$qiniu->uploadFile($_FILES['tmp_name'],$key);
$url = $qiniu->getLink($key);
```
