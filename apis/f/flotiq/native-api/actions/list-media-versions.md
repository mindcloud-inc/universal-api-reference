# List Media Versions with Flotiq

Retrieves versions for a media object in Flotiq.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/_media/{{id}}/version`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [List Media Versions](https://flotiq.com/docs/API/media/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Flotiq media object ID. |
