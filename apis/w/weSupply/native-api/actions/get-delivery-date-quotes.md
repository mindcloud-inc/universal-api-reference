# Get Delivery Date Quotes with WeSupply

Retrieves delivery date quotes from WeSupply.

## Endpoint

- **Method:** `GET`
- **Path:** `/shippingQuotes`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Get Delivery Date Quotes](https://documenter.getpostman.com/view/11859344/T17AiAYq#eb1fb1ec-b48a-4e17-961c-9b23e3372682)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerCountryCode` | query | `string` | no | The destination ISO country code for the quote request. |
| `CustomerPostalCode` | query | `string` | no | The destination postal code for the quote request. |
