# List Automation Sources with Testmo

Retrieves automation sources for a project in Testmo.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/automation/sources`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Automation Sources](https://support.testmo.com/hc/en-us/articles/37974874224141-Automation-Sources)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project whose automation sources should be listed. |
