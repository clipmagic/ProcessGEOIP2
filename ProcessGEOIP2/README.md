# ProcessGEOIP2 V0.0.1


## General information
This module gives you a ProcessWire module wrapper around the MaxMind GEOIP2-php API and database.

This module includes GeoLite2 data created by MaxMind, available from
<a href="http://www.maxmind.com target="_blank">http://www.maxmind.com</a>. This database is updated monthly and it's simply a matter of FTP'ing the latest version to the maxmind-db directory in the module's directory structure. 

By default, it uses the free GeoLite2-Country.mnmdb database. To change the database, you could create a hook to your new database location & name.

## Installation
* Download the zip file into your site/modules folder then expand the zip file
* Login to ProcessWire > go to Modules > click "Refresh". You should see a note that a new module was found. Install the module. 


## Usage
### Basic usage
In your template:

```
<?php 
$geoipMod = $modules->get('ProcessGEOIP2');
$reader = $geoipMod->getReader();
?>
```
From there, your $reader object has access to all the API classes and functions, eg to get the ISO country code of your site visitor:

```
<?php
echo $reader->country->isoCode;
?>
```
Read the API documentation at <a href="https://github.com/maxmind/GeoIP2-php" target="_blank">https://github.com/maxmind/GeoIP2-php</a> for more information.

## Change log
2017-02-04: Initial release, v0.0.1

