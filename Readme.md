# PHP Class

Simply include or require the class file & use. No need to instantiate the class as all methods are static:

```php
require_once '../vendor/autoload.php';
require_once '../src/Detect.php';

// Any mobile device (phones or tablets)
if (Detect\Detect::isMobile()) {
	echo 'is mobile!';
}

// Gets the device type ('Computer', 'Phone' or 'Tablet')
echo Detect\Detect::deviceType();

// Any phone device
if (Detect\Detect::isPhone()) {
	echo 'is phone!';
}

// Any tablet device
if (Detect\Detect::isTablet()) {
	echo 'is tablet!';
}

// Any computer device (desktops or laptops)
if (Detect\Detect::isComputer()) {
	echo 'is computer!';
}

// Get the IP address of the device
echo Detect\Detect::ip();

// Get the ID address host name of the device
echo Detect\Detect::ipHostname();

// Get the IP address organisation of the device
echo Detect\Detect::ipOrg();

// Get the country the IP address is in (IP address location inaccurate)
// (JS function available which uses the Geolocation API)
echo Detect\Detect::ipCountry();

// Get the name & version of operating system
echo Detect\Detect::os();

// Get the name & version of browser
echo Detect\Detect::browser();

// Detect\Detects if IE is version 9 or less & if it is, returns a warning:
// <strong>YOU ARE USING AN OUTDATED BROWSER</strong><br>It is limiting your experience.<br>Please upgrade your browser.
// Optionally, send html to be prepended or appended to warning
echo Detect\Detect::ieOld([$prependHTML = ''],[ $appendHTML = '']);

// Get the brand of device (only works with mobile devices otherwise return null)
echo Detect\Detect::brand();

// Check for a specific platform with the help of the magic methods:
if (Detect\Detect::isiOS()) {

}

if (Detect\Detect::isAndroidOS()) {

}

```

## Copyright
Developed by [Kevin Warren](https://twitter.com/KevinTWarren)

Download of plain version under [detectdevice.com](https://detectdevice.com/#download)

Detect Device is an open-source script released under [MIT License](https://opensource.org/licenses/MIT)
