# Get the time report of the projects and users you manage with Worksnaps

Retrieves managed project time reports from Worksnaps.

## Endpoint

- **Method:** `GET`
- **Path:** `/summary_reports`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Get the time report of the projects and users you manage](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | query | `string` | no | The starting date, in the format of YYYY-mm-dd. |
| `name` | query | `string` | no | this is a constant |
| `project_ids` | query | `string` | no | List of project IDs, separated by semi-colon. (If not specified, all of your managed projects will be used.) |
| `timezone_offset` | query | `string` | no | The timezone offset that is used to determine the timestamp associated with from_date and to_date. For example, 8, -8, +5.5, 0.<br>If not specified, the current user's timezone is used. |
| `to_date` | query | `string` | no | The ending date, in the format of YYYY-mm-dd. <br><br>The difference between from_date and to_date cannot be larger than 30 days. |
| `user_ids` | query | `string` | no | List of user IDs separated by semi-colon. (If not specified, all the users in your managed projects will be used.) |
