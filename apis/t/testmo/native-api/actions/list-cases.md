# List Cases with Testmo

Retrieves cases for a project in Testmo.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/cases`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Cases](https://support.testmo.com/hc/en-us/articles/40051160964749-Cases)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project whose cases should be listed. |
