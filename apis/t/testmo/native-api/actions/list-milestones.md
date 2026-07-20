# List Milestones with Testmo

Retrieves milestones for a project in Testmo.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/milestones`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Milestones](https://support.testmo.com/hc/en-us/articles/38157425816717-Milestones)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project whose milestones should be listed. |
