# List Tags with Rebrandly

Retrieves tags from Rebrandly.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [List Tags](https://developers.rebrandly.com/docs/listing-your-tags)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of tags to return. |
| `orderBy` | query | `string` | no | Field used to sort the tags collection. |
| `orderDir` | query | `string` | no | Sort direction for the tags collection. |
| `last` | query | `string` | no | Cursor: the last tag ID returned by the previous page. |
