# Update Shop with GetResponse

Updates an existing shop in GetResponse.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shopId`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Update Shop](https://apireference.getresponse.com/#operation/updateShop)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shopId` | path | `string` | yes | The shop ID |
| `name` | body | `string` | no | The shop name |
| `locale` | body | `string` | no | The language locale (ISO 639-1) |
| `currency` | body | `string` | no | The currency code (ISO 4217) |
