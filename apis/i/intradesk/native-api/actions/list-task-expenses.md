# List Task Expenses with Intradesk

Retrieves task expenses from Intradesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/taskform/api/v2/TaskExpense/{taskNumber}`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [List Task Expenses](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/TaskExpense/get_api_v2_TaskExpense__taskNumber_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskNumber` | path | `string` | yes | Task number from Intradesk TaskForm API path. |
