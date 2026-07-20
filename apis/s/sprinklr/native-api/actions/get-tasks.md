# Get Tasks with Sprinklr

Retrieves tasks from Sprinklr.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v2/task`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Get Tasks](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Ftask/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of tasks to return. |
| `taskIds` | query | `string` | no | Optional task IDs to fetch. Use the format expected by Sprinklr for one or more task IDs. |
