# List Sessions with Testmo

Retrieves sessions for a project in Testmo.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/sessions`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Sessions](https://support.testmo.com/hc/en-us/articles/38159977518989-Sessions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project whose sessions should be listed. |
