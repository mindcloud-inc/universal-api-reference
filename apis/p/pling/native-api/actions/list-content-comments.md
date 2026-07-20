# List Content Comments with Pling

Retrieves public content comments from Pling.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/data/:type/:contentId/:contentId2`
- **Base URL:** `https://api.pling.com/ocs/v1`
- **Official documentation:** [List Content Comments](https://www.opendesktop.org/ocs-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | OCS comment type. Use 1 for content comments. |
| `contentId` | path | `string` | yes | Pling content identifier whose comments should be listed. |
| `contentId2` | path | `string` | yes | Second OCS identifier segment; use 0 for top-level content comments. |
