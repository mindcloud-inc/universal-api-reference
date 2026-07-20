# List Documents with Documenso

Retrieves documents from Documenso.

## Endpoint

- **Method:** `GET`
- **Path:** `/envelope`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [List Documents](https://docs.documenso.com/docs/developers/api/documents)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `list` | no | Accepted values: `DOCUMENT`, `TEMPLATE`. |
| `status` | query | `list` | no | Accepted values: `COMPLETED`, `DRAFT`, `PENDING`, `REJECTED`. |
| `source` | query | `list` | no | Accepted values: `API`, `DOCUMENT`, `TEMPLATE`. |
| `folderId` | query | `string` | no | — |
