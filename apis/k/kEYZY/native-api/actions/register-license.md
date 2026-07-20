# Register License with KEYZY

Registers a new customer to a KEYZY license.

## Endpoint

- **Method:** `POST`
- **Path:** `/licenses/register`
- **Base URL:** `https://api.keyzy.io/v2`
- **Official documentation:** [Register License](https://www.keyzy.io/docs/developers/rest-api/licenses-register/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Licensee's email address. |
| `end_at` | body | `number` | no | License end time as a Unix timestamp. |
| `name` | body | `string` | yes | Licensee's name. |
| `sku_number` | body | `string` | yes | A sku_number. |
| `start_at` | body | `number` | no | License start time as a Unix timestamp. |
| `type` | body | `string` | no | License type: perpetual, subscription, or trial. |
