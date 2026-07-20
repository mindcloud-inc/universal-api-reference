# Extract Data from Purchase Order with Bitskout

Extracts purchase order data with a Bitskout plugin.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/purchase_order`
- **Base URL:** `https://api.bitskout.com/v2`
- **Official documentation:** [Extract Data from Purchase Order](https://learn.microsoft.com/en-us/connectors/bitskout/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_url` | body | `string` | no | Download URL for the purchase order file to extract. |
