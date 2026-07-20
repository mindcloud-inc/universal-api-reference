# List Links with Dub

Retrieves links from Dub.

## Endpoint

- **Method:** `GET`
- **Path:** `/links`
- **Base URL:** `https://api.dub.co`
- **Official documentation:** [List Links](https://dub.co/docs/api-reference/links/list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search links by text. |
| `domain` | query | `string` | no | Filter links by domain. |
| `withTags` | query | `boolean` | no | Include tag data in list results. |
