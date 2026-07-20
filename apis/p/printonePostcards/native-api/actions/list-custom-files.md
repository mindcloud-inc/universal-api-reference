# List Custom Files with Print.one Postcards

Retrieves custom files from Print.one Postcards.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customfiles`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [List Custom Files](https://api.print.one/docs/v2#operation/CustomFiles/getCustomFileList)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search term to filter custom files |
| `searchBy` | query | `string` | no | Fields to search by |
