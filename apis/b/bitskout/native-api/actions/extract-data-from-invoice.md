# Extract Data from Invoice with Bitskout

Extracts invoice data with a Bitskout plugin.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/invoices`
- **Base URL:** `https://api.bitskout.com/v2`
- **Official documentation:** [Extract Data from Invoice](https://learn.microsoft.com/en-us/connectors/bitskout/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_url` | body | `string` | no | Download URL for the invoice file to extract. |
