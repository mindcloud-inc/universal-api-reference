# Get Trend Analysis For User with PocketSmith

Retrieves trend analysis for a PocketSmith user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/trend_analysis`
- **Base URL:** `https://api.pocketsmith.com/v2`
- **Official documentation:** [Get Trend Analysis For User](https://developers.pocketsmith.com/reference/get_users-id-trend-analysis-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categories` | query | `string` | yes | A comma-separated list of category IDs to analyse. |
| `end_date` | query | `string` | yes | The date to stop analysing the trend at. |
| `id` | path | `number` | yes | The unique identifier of the PocketSmith user. |
| `interval` | query | `number` | yes | The period interval to analyse in. |
| `period` | query | `string` | yes | The period to analyse in. |
| `scenarios` | query | `string` | yes | A comma-separated list of scenario IDs to analyse. |
| `start_date` | query | `string` | yes | The date to start analysing the trend from. |
