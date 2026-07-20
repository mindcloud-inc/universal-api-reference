# List Assigned Tasks with Awork

Retrieves assigned tasks from Awork.

## Endpoint

- **Method:** `GET`
- **Path:** `/me/assignedtasks`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [List Assigned Tasks](https://developers.awork.com/apiv1/assigned-tasks/get-my-me-assigned-tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inProgress` | query | `boolean` | no | Whether to return only tasks currently in progress. |
| `assignedOnFrom` | query | `string` | no | The start date and time for filtering by assignment date. If set, tasks are returned only when the assignment date is greater or equal than this value. |
| `assignedOnTo` | query | `string` | no | The end date and time for filtering by assignment date. If set, tasks are returned only when the assignment date is less or equal than this value. |
