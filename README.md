<h1 align="center"> weather </h1>

<p align="center"> 基于 高德开放平台 的 PHP 天气信息组件.</p>


## Installing

```shell
$ composer require godquan/weather -vvv
```
##配置
在使用本扩展之前，你需要去 高德开放平台 注册账号，然后创建应用，获取应用的 API Key。

## Usage

use GodQuan\weather\weather;

$key = 'xxxxxxxxxxxxxxxxxxxxxxxxxxx';

$weather = new Weather($key);

##获取实时天气
$response = $weather->getWeather('城市名');

##获取近期天气预报
$response = $weather->getWeather('城市名', 'all');

##参数说明
array|string getWeather(string $city, string $type = 'base', string $format = 'json')

$city - 城市名，比如：“深圳”；

$type - 返回内容类型：base: 返回实况天气 / all: 返回预报天气；

$format - 输出的数据格式，默认为 json 格式，当 output 设置为 “xml” 时，输出的为 XML 格式的数据。

## Contributing

You can contribute in one of three ways:

1. File bug reports using the [issue tracker](https://github.com/godquan/weather/issues).
2. Answer questions or fix bugs on the [issue tracker](https://github.com/godquan/weather/issues).
3. Contribute new features or update the wiki.

_The code contribution process is not very formal. You just need to make sure that you follow the PSR-0, PSR-1, and PSR-2 coding guidelines. Any new code contributions must be accompanied by unit tests where applicable._

## License

BY GodQuan