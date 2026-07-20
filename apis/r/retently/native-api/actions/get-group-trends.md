# Get Group Trends with Retently

Retrieves trend data for a group from Retently.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/trends/:groupId`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [Get Group Trends](https://www.retently.com/api/#api-get-trends-group-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Group Id |
| `date` | query | `string` | no | Date range preset supporting the following ptions: today, yesterday, past-week, past-month, past-3-months, past-6-months, past-year, this-month-to-date, this-quarter-to-date, this-year-to-date, custom. |
| `startDate` | query | `string` | no | Custom start date in ISO format or UNIX timestamp. |
| `endDate` | query | `string` | no | Custom end date in ISO format or UNIX timestamp. |
