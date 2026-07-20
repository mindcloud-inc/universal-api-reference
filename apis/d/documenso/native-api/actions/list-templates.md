# List Templates with Documenso

Retrieves templates from Documenso.

## Endpoint

- **Method:** `GET`
- **Path:** `/template`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [List Templates](https://docs.documenso.com/docs/developers/api/templates)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `list` | no | Accepted values: `PRIVATE`, `PUBLIC`. |
| `folderId` | query | `string` | no | — |
