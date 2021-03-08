# Laravel YAML

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/athmarios/laravel-yaml/master/LICENSE) 

This package will allow your application to determine whether the request wants a YAML response and then also respond with YAML. Made to work for laravel 8.

## Install

You can pull in the package via composer:
``` bash
$ composer require athmarios/yaml-response
```

## Usage

See if the request wants a YAML response and then respond with YAML...

```php
// app/Http/routes.php

use Illuminate\Http\Request;

Route::get('/some/route', function (Request $request) {
	// Was this a YAML request?
	if ($request->wantsYaml()) {
		// Then let's respond with YAML!
		response()->yaml(['This is my YAML response!']);
	}
});
```

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
