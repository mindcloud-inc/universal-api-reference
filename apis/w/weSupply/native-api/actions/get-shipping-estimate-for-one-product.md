# Get Shipping Estimate For One Product with WeSupply

Retrieves a shipping estimate from WeSupply for one product.

## Endpoint

- **Method:** `POST`
- **Path:** `/shippingEstimate`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Get Shipping Estimate For One Product](https://documenter.getpostman.com/view/11859344/T17AiAYq#983ca975-a4c2-43d8-82f1-f622397efeac)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LocationType` | body | `string` | no | The lookup mode for the shipping estimate, such as zip code. |
| `RequestID` | body | `string` | no | A caller-provided identifier for the shipping estimate request. |
| `ZipCode` | body | `string` | no | The destination postal code for the shipping estimate. |
