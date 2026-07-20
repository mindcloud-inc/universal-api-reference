# Extract Data from HARO Query with Bitskout

Extracts HARO query data with a Bitskout plugin.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/haro`
- **Base URL:** `https://api.bitskout.com/v2`
- **Official documentation:** [Extract Data from HARO Query](https://learn.microsoft.com/en-us/connectors/bitskout/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | no | HARO query text to extract structured details from. |
