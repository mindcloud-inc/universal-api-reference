# Create Shop with GetResponse

Creates a new shop in GetResponse.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Create Shop](https://apireference.getresponse.com/#operation/createShop)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The shop name |
| `locale` | body | `string` | yes | The language locale (ISO 639-1) |
| `currency` | body | `string` | yes | The currency code (ISO 4217) |
