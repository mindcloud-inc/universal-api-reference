# List Folders with Testmo

Retrieves folders for a project in Testmo.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/folders`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Folders](https://support.testmo.com/hc/en-us/articles/40067196221837-Folders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project whose folders should be listed. |
