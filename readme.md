# Update (10 March 2025)
I fixed Phalcon's GitHub Actions with [this pull request](https://github.com/phalcon/cphalcon/pull/16533) - Thereby fixing the auto-compiled DLLs with each release and effectively making this repo redundant. It was my intention to post an update here much earlier but I got sidetracked and forgot. 

This repo will remain here as an archive, but any and all DLLs should be downloaded directly from either a.) Phalcon's official GitHub releases or b.) from the PECL repo website.

# Pre-Compiled Phalcon DLL Files

For those that are not aware, on [17 Oct 2022](https://windows.php.net/#news-2022-10-17-1) the PHP Team posted a news update stating that the Windows PECL build machine died, and that they are still working on a permanent solution for building DLLs for PECL extensions with a new CI process. In the meantime, this presents some difficulties on Phalcon developers using windows, as the process to compile an extension for PHP is not an easy or quick task, and using WSL is not always an option for everyone. With some studying, I was able to get my own Phalcon extension compiled, so I wanted to share that for those who have been stuck using an outdated version of Phalcon.

Here you will find a list of pre-compiled DLL files of the Phalcon PHP Framework to use on your Windows environment. All you need to do is locate the appropriate DLL file for your PHP version, place it into your extension directory and enable it.

Note: In order for the Phalcon extension to work properly, [the following steps should be followed from the official Phalcon documentation](https://docs.phalcon.io/latest/installation/#php-80):

> ### Load order
> 
> Phalcon needs to be loaded after  `PDO`. Some distributions add a
> number prefix on  `ini`  files. If that is the case, choose a high
> number for Phalcon (e.g.  `50-phalcon.ini`), higher than  `PDO`. This
> will load Phalcon after the prerequisite extensions. If however, your
> distribution only has a  `php.ini`  file, please make sure that the
> order is similar to this:
> 
>     extension=pdo.so
>     extension=phalcon.so
> 
> 
> Along with PHP 8.0 or greater, depending on your application needs and
> the Phalcon components you need, you might need to install the
> following extensions:
> 
> -   [curl](https://www.php.net/manual/en/book.curl.php)
> -   [fileinfo](https://www.php.net/manual/en/book.fileinfo.php)
> -   [gettext](https://www.php.net/manual/en/book.gettext.php)
> -   [gd2](https://www.php.net/manual/en/book.image.php)  (to use the  [Phalcon\Image\Adapter\Gd](https://docs.phalcon.io/latest/api/phalcon_image/#image-adapter-gd)
> class)
> -   [imagick](https://www.php.net/manual/en/book.imagick.php)  (to use the 
> [Phalcon\Image\Adapter\Imagick](https://docs.phalcon.io/latest/api/phalcon_image/#image-adapter-imagick)
> class)
> -   [json](https://www.php.net/manual/en/book.json.php)
> -   `libpcre3-dev`  (Debian/Ubuntu),  `pcre-devel`  (CentOS),  `pcre`  (macOS)
> -   [PDO](https://php.net/manual/en/book.pdo.php)  Extension as well as the relevant RDBMS-specific extension (i.e. 
> [MySQL](https://php.net/manual/en/ref.pdo-mysql.php), 
> [PostgreSql](https://php.net/manual/en/ref.pdo-pgsql.php), etc.)
> -   [OpenSSL](https://php.net/manual/en/book.openssl.php)  Extension
> -   [Mbstring](https://php.net/manual/en/book.mbstring.php)  Extension
> -   [Memcached](https://php.net/manual/en/book.memcached.php)  or other relevant cache adapters depending on your usage of cache


## Folder Structure in this Repository

As of 13 February 2024, I have included pre-compiled DLLs of the latest version of the Phalcon Framework for each of the following official releases of PHP:

 - **PHP 8.3 (8.3.2)**
     - VS16 x64 Non Thread Safe
     - VS16 x64 Thread Safe
     - VS16 x86 Non Thread Safe
     - VS16 x86 Thread Safe

- **PHP 8.2 (8.2.15)**
     - VS16 x64 Non Thread Safe
     - VS16 x64 Thread Safe
     - VS16 x86 Non Thread Safe
     - VS16 x86 Thread Safe

- **PHP 8.1 (8.1.27)**
     - VS16 x64 Non Thread Safe
     - VS16 x64 Thread Safe
     - VS16 x86 Non Thread Safe
     - VS16 x86 Thread Safe

To navigate and find the correct version that you need, use your PHP version as a reference:
If for example your version of PHP is **php-8.2.15-nts-Win32-vs16-x64**, then you would find your DLL at:

**[Phalcon Version]** -> **php8.2-vs16** -> **x64** -> **nts**


## Future Compiled Versions

In the near future, I will incrementally release updates to this repository for older versions of Phalcon for all of the applicable PHP versions.

Following the official PHP support lifecycle, I will not be compiling Phalcon framework DLLs for versions older than PHP 8.1 and PHP 8.1 will be dropped from my compiling queue on 25 Nov 2024, when the official security support of that version ends.

As the Phalcon team releases new versions of the framework, I will update this repository as quickly as I can to provide myself and all of you with the DLL file needed for your version of PHP.

## Need a different extension compiled? I'm happy to help!

If there is another extension you need compiled other than Phalcon, you can reach me by email at justin@justinmoody.com or via discord (Username: saintisaiah) 

## Feeling Generous? Buy Me a Coffee

If you appreciate this work and would like to buy me a cup of coffee, you can [send me a donation on PayPal](https://paypal.me/jmoodyfwd). 
No donations are required, but greatly appreciated. :)
