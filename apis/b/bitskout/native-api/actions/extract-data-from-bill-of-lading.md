# Extract Data from Bill of Lading with Bitskout

Extracts bill of lading data with a Bitskout plugin.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/bill_of_lading`
- **Base URL:** `https://api.bitskout.com/v2`
- **Official documentation:** [Extract Data from Bill of Lading](https://learn.microsoft.com/en-us/connectors/bitskout/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_url` | body | `string` | no | Direct download URL for the bill of lading file to extract. |
