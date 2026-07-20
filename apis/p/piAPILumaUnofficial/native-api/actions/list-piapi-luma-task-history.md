# List PiAPI Luma Task History with PiAPI/Luma (unofficial)

Retrieves Luma task history from PiAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/open/tasks/histories`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [List PiAPI Luma Task History](https://piapi.ai/docs/piapi-user-history-query)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_time` | query | `number` | no | Optional Unix timestamp lower bound for task-history results. |
| `end_time` | query | `number` | no | Optional Unix timestamp upper bound for task-history results. |
