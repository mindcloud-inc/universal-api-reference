# List Spaces with Google Chat

Retrieves Google Chat spaces the caller is a member of.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces`
- **Base URL:** `https://chat.googleapis.com/v1`
- **Official documentation:** [List Spaces](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Optional. Filter spaces by supported Google Chat space fields. |
