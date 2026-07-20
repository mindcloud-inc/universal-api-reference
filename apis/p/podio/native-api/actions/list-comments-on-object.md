# List Comments on Object with Podio

Retrieves comments on a Podio object.

## Endpoint

- **Method:** `GET`
- **Path:** `/comment/:type/:id/`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [List Comments on Object](https://developers.podio.com/doc/comments/get-comments-on-object-22371)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | The type of object to read comments from. |
| `id` | path | `string` | yes | The ID of the object to read comments from. |
