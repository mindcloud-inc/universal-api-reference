# Get List of Activities with Zixflow

Retrieves activities from Zixflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/collection-records/activity-list/query`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Get List of Activities](https://docs.zixflow.com/api-reference/activity-list/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[]` | body | `array` | no | Filter array for activity query. |
| `sort[]` | body | `array` | no | Sort instructions for activity query. |
| `limit` | body | `number` | no | Maximum number of activities to return. |
| `offset` | body | `number` | no | Number of activities to skip. |
