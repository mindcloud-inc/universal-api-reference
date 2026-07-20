# List Comments with Frame.io v4

Retrieves comments for a file in Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/files/:fileId/comments`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [List Comments](https://next.developer.frame.io/platform/api-reference/comments/index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `file_id` | path | `string` | yes |
| `timestamp_as_timecode` | query | `boolean` | no |
| `include` | query | `string` | no |
