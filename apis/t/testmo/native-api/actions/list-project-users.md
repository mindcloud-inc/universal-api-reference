# List Project Users with Testmo

Retrieves users for a project in Testmo.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/users`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Project Users](https://support.testmo.com/hc/en-us/articles/38165363497741-Users)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project whose users should be listed. |
