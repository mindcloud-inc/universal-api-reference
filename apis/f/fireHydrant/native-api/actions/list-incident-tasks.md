# List Incident Tasks with FireHydrant

Retrieves incident tasks from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents/:incident_id/tasks`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Incident Tasks](https://docs.firehydrant.com/reference/list_incident_tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incident_id` | path | `string` | yes | The FireHydrant incident ID. |
