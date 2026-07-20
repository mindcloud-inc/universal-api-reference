# Update Task with Wodely

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/tasks/[:taskGuid]`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Update Task](https://app.wodely.com/doc/api-documentation.html#update-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskGuid` | path | `string` | yes | Task identifier returned by Wodely. |
| `taskDesc` | body | `string` | no | Updated task description. |
| `destinationAddress` | body | `string` | no | Updated full destination address. |
| `alert` | body | `string` | no | Set `N` to disable email and SMS notifications. |
