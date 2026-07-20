# Get Task History Comment with Intradesk

Retrieves a task history comment from Intradesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/taskhistory/api/v3/Lifetime/{taskId}/{historyUid}/comment`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [Get Task History Comment](https://apigw.intradesk.ru/taskhistory_docs/swagger/index.html#/Lifetime/get_api_v3_Lifetime__taskId___historyUid__comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Task identifier from Intradesk TaskHistory API path. |
| `historyUid` | path | `string` | yes | History entry UID from Intradesk TaskHistory API path. |
