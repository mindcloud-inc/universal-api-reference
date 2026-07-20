# Get Task Type Fields with Intradesk

Retrieves task type fields from Intradesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/taskform/api/TaskTypes/{ids}/fields`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [Get Task Type Fields](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/TaskTypes/get_api_TaskTypes__ids__fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | One or more task type identifiers from the Intradesk TaskForm API path. Send multiple values as a string separated by `,`. |
