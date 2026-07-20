# List Task History with Intradesk

Retrieves task history entries from Intradesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/taskhistory/api/v3/Lifetime/{taskid}/full`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [List Task History](https://apigw.intradesk.ru/taskhistory_docs/swagger/index.html#/Lifetime/get_api_v3_Lifetime__taskid__full)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskid` | path | `string` | yes | Task identifier from Intradesk TaskHistory API path. |
