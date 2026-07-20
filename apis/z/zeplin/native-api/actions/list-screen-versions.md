# List Screen Versions with Zeplin

Retrieves a list of screen versions from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/screens/{screen_id}/versions`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Screen Versions](https://docs.zeplin.dev/reference/getscreenversions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
