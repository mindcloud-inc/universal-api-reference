# Complete Task with Zoho Connect

Completes a task in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/completeTask`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Complete Task](https://www.zoho.com/connect/api/complete-task.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | ID of the network where the task exists. |
| `taskId` | query | `string` | yes | ID of the task to complete. |
