# List Surveys with PickFu

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys`
- **Base URL:** `https://api.pickfu.com/v1`
- **Official documentation:** [List Surveys](https://www.pickfu.com/docs/api-reference/surveys/list-surveys)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter surveys by status. |
| `type` | query | `string` | no | Filter surveys by question type. |
| `option_type` | query | `string` | no | Filter surveys by option type. |
| `countries` | query | `string` | no | Filter surveys by country codes. Send multiple values as a string separated by `,`. |
| `tags` | query | `string` | no | Filter surveys by tag IDs. Send multiple values as a string separated by `,`. |
| `audiences` | query | `string` | no | Filter surveys by audience IDs. Send multiple values as a string separated by `,`. |
| `text` | query | `string` | no | Search survey names and questions. |
| `member_id` | query | `string` | no | Filter surveys by team member ID. Send multiple values as a string separated by `,`. |
| `project_ids` | query | `string` | no | Filter surveys by project IDs. Send multiple values as a string separated by `,`. |
| `published_after` | query | `date` | no | Only include surveys published after this ISO 8601 datetime. |
| `sort_by` | query | `string` | no | Sort surveys by the selected field. |
| `dir` | query | `string` | no | Sort direction. |
