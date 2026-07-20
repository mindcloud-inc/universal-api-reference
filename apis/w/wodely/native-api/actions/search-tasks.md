# Search Tasks with Wodely

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks/search`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Search Tasks](https://app.wodely.com/doc/api-documentation.html#list-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDateTime` | body | `string` | yes | UTC ISO 8601 start of the search window. |
| `endDateTime` | body | `string` | yes | UTC ISO 8601 end of the search window. |
| `taskStatusId` | body | `string` | no | Filter tasks by Wodely task status identifier. |
| `taskTypeId` | body | `string` | no | Filter tasks by Wodely task type identifier. |
| `teamId` | body | `string` | no | Filter tasks by team identifier. |
| `driverUserId` | body | `string` | no | Filter tasks by assigned driver user identifier. |
| `merchantId` | body | `string` | no | Filter tasks by merchant identifier. |
| `taskGuid` | body | `string` | no | Filter by the task GUID. |
| `externalKey` | body | `string` | no | Filter by the external task key. |
| `routeId` | body | `string` | no | Filter tasks by route identifier. |
| `limit` | body | `number` | no | Maximum number of tasks to return. |
| `lastId` | body | `string` | no | Cursor value from the previous response for pagination. |
