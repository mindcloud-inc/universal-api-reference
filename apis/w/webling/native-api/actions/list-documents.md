# List Documents with Webling

## Endpoint

- **Method:** `GET`
- **Path:** `/document`
- **Base URL:** `https://{instanceDomain}/api/1`
- **Official documentation:** [List Documents](https://demo.webling.ch/api/1#document-document-list-get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Filter the document list using Webling query language. |
| `order` | query | `string` | no | Sort the document list by property and direction. |
| `format` | query | `string` | no | Use full to return full document objects instead of IDs. |
