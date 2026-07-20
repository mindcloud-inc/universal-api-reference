# List Runs with Testmo

Retrieves runs for a project in Testmo.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/runs`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Runs](https://support.testmo.com/hc/en-us/articles/38159162797197-Runs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project whose runs should be listed. |
