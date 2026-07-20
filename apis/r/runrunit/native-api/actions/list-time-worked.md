# List Time Worked with Runrun.it

Retrieves time worked reports from Runrun.it.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/time_worked`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [List Time Worked](https://runrun.it/api/documentation#time-worked-list-all-time-worked-grouped-and-filtered-by-parameters)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_capacity` | query | `boolean` | no | Include capacity |
| `include_untracked` | query | `boolean` | no | Include untracked |
| `include_others` | query | `boolean` | no | Include others |
| `expand_others` | query | `boolean` | no | Expand others field to a non-aggregate |
| `group_by` | query | `string` | no | Attributes to group by: date, client_id, project_group_id, project_id, project_sub_group_id, task_id, task_status_id, team_id, type_id, user_id |
| `period_type` | query | `string` | no | Period type. Must be one of the following: last_seven_days, current_week, last_fifteen_days, last_thirty_days, current_month, last_ninety_days, current_quarter, last_one_year, custom_range |
| `period_start` | query | `date` | no | Period start. Only used if period_type is 'custom_range' |
| `period_end` | query | `date` | no | Period end. Only used if period_type is 'custom_range' |
| `period_unit` | query | `string` | no | Period unit. Must be one of the following: day, week, month or year |
| `client_id` | query | `string` | no | IDs of clients, separated by comma |
| `project_id` | query | `string` | no | IDs of projects, separated by comma |
| `project_group_id` | query | `string` | no | ID of project group |
| `project_subgroup_id` | query | `string` | no | ID of project subgroup |
| `tag_list` | query | `string` | no | List of task tags, separated by comma |
| `type_id` | query | `string` | no | IDs of task types, separated by comma |
| `team_id` | query | `string` | no | IDs of teams, separated by comma |
| `user_id` | query | `string` | no | IDs of users, separated by comma |
