
# Mailazy SDK for PHP
This repository contains the open source PHP SDK that allows you to access the Mailazy Platform from your PHP app.

Please visit [mailazy.com](https://mailazy.com/) for more information.

# Quickstart Guide

## Installation

The Mailazy PHP SDK can be installed with  [Composer](https://getcomposer.org/). Run this command:
```
composer require mailazy/php-sdk
```

## Configuration
After successful install, you need to define the following Mailazy Account info in your project anywhere before using the Mailazy SDK or in the config file of your project:

### Usage

```
<?php
define('MAILAZY_APIKEY','xxxxxxxxxxxxxxxxxxxxxxxx');// mailazy apikey replace at "MAILAZY_APIKEY"
define('MAILAZY_APISECRET','xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx');// mailazy apikey replace at "MAILAZY_APISECRET"

require 'vendor/autoload.php';

$mailazyClient = new mailazyAPI();
$mailazyClient->setApikey(MAILAZY_APIKEY);
$mailazyClient->setApisecret(MAILAZY_APISECRET);
$mailazyClient->isHTML(true);
$mailazyClient->addAddress($email,$userName);
//Set CC address
$mailazyClient->addCC($email,$userName);
//Set BCC address
$mailazyClient->addBCC($email,$userName);
$mailazyClient->setSubject($subject);
$mailazyClient->setBody($message);
$mailazyClient->setFrom($senderEmail,$sendername);
$mailazyClient->addReplyTo($replyEmail,$replyname);
$mailazyClient->addAttachment($filePath);
$mailazyClient->send();
```          

## License

Please see the  [license file](https://github.com/mailazy/mailazy-php/blob/master/LICENSE)  for more information.      

## Documentation

[Getting Started](https://mailazy.com/docs/) - Everything you need to begin using this SDK.