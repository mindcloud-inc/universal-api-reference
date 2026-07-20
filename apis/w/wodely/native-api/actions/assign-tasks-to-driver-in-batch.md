# Assign Tasks to Driver in Batch with Wodely

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks/driver`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Assign Tasks to Driver in Batch](https://app.wodely.com/doc/api-documentation.html#assign-task-to-driver)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignments[].taskGuid` | body | `string` | yes | Task Id. |
| `assignments[].driverUserId` | body | `string` | yes | Driver user id, username, or email. |
