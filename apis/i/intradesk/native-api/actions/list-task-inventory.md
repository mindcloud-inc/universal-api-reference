# List Task Inventory with Intradesk

Retrieves task inventory from Intradesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/taskform/api/TaskInventory/{taskId}`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [List Task Inventory](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/TaskInventory/get_api_TaskInventory__taskId_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Task identifier from Intradesk TaskForm API path. |
