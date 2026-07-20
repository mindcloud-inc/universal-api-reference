# Copy Task with Intradesk

Copies an existing task in Intradesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/changes/v1/Tasks/Copy`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [Copy Task](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Tasks/post_v1_Tasks_Copy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | TaskFormCopyModel JSON object request body documented by Intradesk Changes API. |
