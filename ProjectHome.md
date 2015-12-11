# NOTICE #
This lib is not supported officially by Google, it was developed by a PHP developer that is not related with Google in any mater.  You need to comply with Google terms of use for the Ajax Language Translate api ([http://code.google.com/apis/ajaxlanguage/terms.html](http://code.google.com/apis/ajaxlanguage/terms.html))

# GTranslate #
Google Translate™ API PHP Wrapper

## About ##
PHP library that wraps the Google Translate™ API. Translates a phrase from one language to another.

## Download ##
[GTranslate 0.7.9.1](http://gtranslate-api-php.googlecode.com/files/gtranslate-api-php-0.7.9.1.zip)

## ChangeLog ##
  * 0.7.9.1 [13 2011](April.md)
    * Removed ' from languages.v2.ini in order to manage compatibility with php < 5.3
    * Added more examples into example.php
  * 0.7.9 [13 2011](April.md)
    * Applied improvements sent by (Azhari Harahap)
      * Removing notice Notice: Undefined index:  HTTP\_REFERER when runing script from console
      * Created a setLanguageFile($file) method to define language file to use
  * 0.7.8 [21 2010](Jan.md):
    * Fixed issues on languages file [35](35.md)
  * 0.7.7:
    * Updated languages file, issue [28](28.md)
    * Updated version on GTranslate.php, issue [29](29.md)
    * Fixed the issue that was preventing Nowergian translation to be done, issue [26](26.md)
    * Added Referrer parameter setter, issue [22](22.md)
  * 0.7.6:
    * - Bug fixing
      * Afrikaans support fix, issue [24](24.md)
    * - Added functionalities
      * Irish support, issue [16](16.md)
      * userip parameter supported, issue [17](17.md)
  * 0.7.5:
    * - Adding Lib into zip file, no code changes, issue [9,13]
  * 0.7.4:
    * - Fixed Warning when no $_SERVER['HTTP\_REFERER'] is set, issue [5](5.md)
  * 0.7.3:
    * - Fixed requestCurl method in order to allow POST action, this way you can translate bigger chunks of text
  * 0.7.2:
    * - Added support for Google Translate api key parameter
  * 0.7.1:
    * - Added TM to protected brand word
  * 0.7.0 (11/01/2009):
    * - Initial release for the Google Translate™ API PHP Wrapper_

## Usage ##

```
<?php
require("GTranslate.php");

 try{
       $gt = new Gtranslate;
       echo "Translating [Hello World] from English to German => ".$gt->english_to_german("hello world")."<br/>";
        echo "Translating [Ciao mondo] Italian to English => ".$gt->it_to_en("Ciao mondo")."<br/>";
 } catch (GTranslateException $ge)
 {
       echo $ge->getMessage();
 }
?>
```