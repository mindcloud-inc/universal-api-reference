# List Worker Tasks with Onfleet

Retrieves tasks assigned to a worker in Onfleet.

## Endpoint

- **Method:** `GET`
- **Path:** `/workers/:workerId/tasks`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [List Worker Tasks](https://docs.onfleet.com/reference/list-workers-assigned-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workerId` | path | `string` | yes | The Onfleet worker ID. |
