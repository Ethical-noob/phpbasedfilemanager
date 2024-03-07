# File Manager By Ethicalnoob

A good solution for managing files and folders for developers who can't access their site over SSH or FTP 
or else use it as a minishell.

![PHP File Manager](https://raw.github.com/Ethical-noob/phpbasedfilemanager/master/ss.png)

**WARNING! Do not use this script as a regular file manager in public area.
After all actions you must delete this script from the server.**

## Requirements

- PHP 5.7 or higher.

## How to use

Download ZIP with the latest version from the master branch.

Copy **enoob.php** to your website folder and open it in a web browser
(e.g. http://yoursite/any_path/enoob.php).

## Security

Default username/password: **Enoob**/**Enoob**

**Warning! Please set your own username and password in `$auth_users` before use.**

To enable or disable authentication set `$use_auth` to `true` or `false`.

*For better security enable HTTP Authentication in your web server.*

## Embedding

You can include file manager in another script. Just define `FM_EMBED` and other necessary constants. Example:

```php
class SomeController
{
    public function actionIndex()
    {
        define('FM_EMBED', true);
        define('FM_SELF_URL', UrlHelper::currentUrl()); // must be set if URL to manager not equal PHP_SELF
        require 'path/to/enoob.php';
    }
}
```

Supported constants:

- `FM_ROOT_PATH` - default is `$_SERVER['DOCUMENT_ROOT']`
- `FM_ROOT_URL` - default is `'http(s)://site.domain/'`
- `FM_SELF_URL` - default is `'http(s)://site.domain/' . $_SERVER['PHP_SELF']`
- `FM_ICONV_INPUT_ENC` - default is `'CP1251'`
- `FM_USE_HIGHLIGHTJS` - default is `true`
- `FM_HIGHLIGHTJS_STYLE` - default is `'vs'`
- `FM_DATETIME_FORMAT` - default is `'d.m.y H:i'`


## Bug tracker

If you have any issues with file manager, you may report them on
[Issue tracker](https://github.com/Ethical-noob/phpbasedfilemanager/issues).

