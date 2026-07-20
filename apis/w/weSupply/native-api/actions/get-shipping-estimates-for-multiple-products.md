# Get Shipping Estimates For Multiple Products with WeSupply

Retrieves shipping estimates from WeSupply for multiple products.

## Endpoint

- **Method:** `POST`
- **Path:** `/shippingEstimates`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Get Shipping Estimates For Multiple Products](https://documenter.getpostman.com/view/11859344/T17AiAYq#d465f074-9be3-43e8-9350-ed798bfad514)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LocationType` | body | `string` | no | The lookup mode for the shipping estimate, such as zip code. |
| `RequestID` | body | `string` | no | A caller-provided identifier for the shipping estimate request. |
| `ZipCode` | body | `string` | no | The destination postal code for the shipping estimate. |
