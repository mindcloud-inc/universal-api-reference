# Query Profiles with Mixpanel

Retrieves profiles from Mixpanel.

## Endpoint

- **Method:** `POST`
- **Path:** `/query/engage`
- **Base URL:** `https://mixpanel.com/api`
- **Official documentation:** [Query Profiles](https://developer.mixpanel.com/reference/engage-query)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Required when authenticating with a Mixpanel service account. |
| `workspace_id` | query | `number` | no | Optional Mixpanel workspace ID. |
| `distinct_id` | body | `string` | no | Single distinct ID to retrieve. |
| `distinct_ids` | body | `string` | no | JSON array string of distinct IDs to retrieve. |
| `data_group_id` | body | `string` | no | Group key ID when querying group profiles. |
| `where` | body | `string` | no | Expression used to filter users or groups. |
| `output_properties` | body | `list<string>` | no | List of profile properties to return. |
| `session_id` | body | `string` | no | Session identifier from a previous query for paging. |
| `page` | body | `number` | no | Page number starting at zero. |
| `behaviors` | body | `number` | no | Behavior selector used for profile exports. |
| `as_of_timestamp` | body | `number` | no | Timestamp used with `behaviors` paging. |
| `filter_by_cohort` | body | `string` | no | JSON object string like {"id":12345}. |
| `include_all_users` | body | `boolean` | no | Include users without profiles when filtering by cohort. |
