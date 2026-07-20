# List Publication Posts with Beehiiv

Retrieves publication posts from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/posts`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [List Publication Posts](https://developers.beehiiv.com/api-reference/posts/index)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
