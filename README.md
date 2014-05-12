Nginx IP2Location module
------------------------

Description:
------------

The Nginx IP2Location module enables user to easily perform client's IP to geographical location lookup by using IP2Location database.

The IP2Location database can be downloaded from http://lite.ip2location.com (Free) or http://www.ip2location.com (Commercial).


Installation:
------------

1. Download IP2location C library from http://www.ip2location.com/developers/c
2. Change the path to IP2Location library in "ngx_http_ip2location_module.c".
3. Re-compile Nginx from source to include this module. Add the below directive into the compile of Nginx:
   ./configure --add-module=/absolute/path/to/nginx-ip2location-1.0
4. make
5. make install


Usage:
-----

Change your Nginx config file to include the 'ip2location_database' directive:

	ip2location_database /absolute/path/to/IP2LOCATION-LITE-DB1.BIN;


The following variables will be made available in Nginx:

	$ip2location_country_code
	$ip2location_country_name

	
Support
-------
Please visit us at http://www.ip2location.com for services and databases we offer.

For support, please email us at support@ip2location.com
