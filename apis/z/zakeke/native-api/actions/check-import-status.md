# Check Import Status with Zakeke

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/csv/importingresult/:taskID`
- **Base URL:** `https://api.zakeke.com`
- **Official documentation:** [Check Import Status](https://api-reference.zakeke.com/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskID` | path | `number` | yes | Task identifier returned by Import Products Via CSV. |
