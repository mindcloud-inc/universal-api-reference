# Extract Data from Business Cards with Bitskout

Extracts business card data with a Bitskout plugin.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/business_cards`
- **Base URL:** `https://api.bitskout.com/v2`
- **Official documentation:** [Extract Data from Business Cards](https://learn.microsoft.com/en-us/connectors/bitskout/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_url` | body | `string` | no | Direct download URL for the business card image or document. |
