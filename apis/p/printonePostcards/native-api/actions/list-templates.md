# List Templates with Print.one Postcards

Retrieves templates from Print.one Postcards.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/templates`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [List Templates](https://api.print.one/docs/v2#operation/Template/getTemplateList)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search term. |
| `searchBy` | query | `string` | no | Fields to search by. |
| `labels` | query | `string` | no | Deprecated comma-separated labels filter. |
| `formats` | query | `string` | no | Deprecated comma-separated formats filter. |
