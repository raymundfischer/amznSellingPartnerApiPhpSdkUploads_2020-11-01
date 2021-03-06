# amznSellingPartnerApiPhpSdkUploads_2020-11-01
The Selling Partner API for Uploads provides operations that support uploading files.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 2020-11-01
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen
For more information, please visit [https://sellercentral.amazon.com/gp/mws/contactus.html](https://sellercentral.amazon.com/gp/mws/contactus.html)

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/raymundfischer/amznsellingpartnerapiphpsdkuploads_2020-11-01.git"
    }
  ],
  "require": {
    "raymundfischer/amznsellingpartnerapiphpsdkuploads_2020-11-01": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/amznSellingPartnerApiPhpSdkUploads_2020-11-01/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new amznSellingPartnerApiPhpSdk\Uploads_2020-11-01\Api\UploadsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$marketplace_ids = array("marketplace_ids_example"); // string[] | A list of marketplace identifiers. This specifies the marketplaces where the upload will be available. Only one marketplace can be specified.
$content_md5 = "content_md5_example"; // string | An MD5 hash of the content to be submitted to the upload destination. This value is used to determine if the data has been corrupted or tampered with during transit.
$resource = "resource_example"; // string | The URL of the resource for the upload destination that you are creating. For example, to create an upload destination for a Buyer-Seller Messaging message, the {resource} would be /messaging and the path would be  /uploads/v1/uploadDestinations/messaging
$content_type = "content_type_example"; // string | The content type of the file to be uploaded.

try {
    $result = $apiInstance->createUploadDestinationForResource($marketplace_ids, $content_md5, $resource, $content_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UploadsApi->createUploadDestinationForResource: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *https://sellingpartnerapi-na.amazon.com/*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*UploadsApi* | [**createUploadDestinationForResource**](docs/Api/UploadsApi.md#createuploaddestinationforresource) | **POST** /uploads/2020-11-01/uploadDestinations/{resource} | 

## Documentation For Models

 - [CreateUploadDestinationResponse](docs/Model/CreateUploadDestinationResponse.md)
 - [Error](docs/Model/Error.md)
 - [ErrorList](docs/Model/ErrorList.md)
 - [UploadDestination](docs/Model/UploadDestination.md)

## Documentation For Authorization

 All endpoints do not require authorization.


## Author



