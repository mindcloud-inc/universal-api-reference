# List Automation Runs with Testmo

Retrieves automation runs for a project in Testmo.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/automation/runs`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Automation Runs](https://support.testmo.com/hc/en-us/articles/37971158770957-Automation-Runs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project whose automation runs should be listed. |
