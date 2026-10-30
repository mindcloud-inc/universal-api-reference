# Create Site with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/sites`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Create Site](https://api.gocanvas.com/api/v3/docs#create-a-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `address` | body | `string` | no | — |
| `city` | body | `string` | no | — |
| `state` | body | `string` | no | — |
| `zip_code` | body | `string` | no | — |
| `country` | body | `string` | no | Two-letter country abbreviation. Maximum length: 2. |
| `code` | body | `string` | no | — |
| `customer_id` | body | `number` | no | — |
