# Set Task Active State with Intradesk

Sets a task's active state in Intradesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/changes/v1/Tasks/Activate`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [Set Task Active State](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Tasks/post_v1_Tasks_Activate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | TaskActivationInputModel JSON object request body documented by Intradesk Changes API. |
