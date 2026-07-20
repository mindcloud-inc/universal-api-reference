# Update License SKU with KEYZY

Updates the connected SKU for a KEYZY license.

## Endpoint

- **Method:** `POST`
- **Path:** `/licenses/update-sku`
- **Base URL:** `https://api.keyzy.io/v2`
- **Official documentation:** [Update License SKU](https://www.keyzy.io/docs/developers/rest-api/licenses-update-sku/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `current_sku_number` | body | `string` | yes | Current SKU number. |
| `new_sku_number` | body | `string` | yes | New SKU number. |
| `serial` | body | `string` | yes | License serial number. |
