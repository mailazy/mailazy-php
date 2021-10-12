# PHP-SDK
PHP SDK based on Mailazy APIs.

## Introduction

Mailazy PHP is a wrapper which provides access to Mailazy Platform APIs.

Please visit [here](https://mailazy.com/) for more information.

# Quickstart Guide

## Configuration
After successful install, you need to define the following Mailazy Account info in your project anywhere before using the Mailazy SDK or in the config file of your project:

```
<?php
define('MAILAZY_APIKEY','xxxxxxxxxxxxxxxxxxxxxxxx');// mailazy apikey replace at "MAILAZY_APIKEY"
define('MAILAZY_APISECRET','xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx');// mailazy apikey replace at "MAILAZY_APISECRET"

require_once(__DIR__."/mailazyAPI.php");

$mailazyClient = new mailazyAPI();
$mailazyClient->setApikey(MAILAZY_APIKEY);
$mailazyClient->setApisecret(MAILAZY_APISECRET);
$mailazyClient->IsHTML(true);
$mailazyClient->AddAddress($email,$userName);
$mailazyClient->setSubject($subject);
$mailazyClient->setBody($message);
$mailazyClient->setFrom($senderEmail,$sendername);
$mailazyClient->addReplyTo($replyEmail,$replyname);
$mailazyClient->send();
```                

## Documentation

[Getting Started](https://mailazy.com/docs/) - Everything you need to begin using this SDK.