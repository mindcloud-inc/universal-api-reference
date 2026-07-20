# List Project Videos with Vimeo

Retrieves videos in a Vimeo project.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id/projects/:project_id/videos`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List Project Videos](https://developer.vimeo.com/api/reference/folders#get_project_videos)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user. |
| `project_id` | path | `number` | yes | The ID of the folder. |
| `query` | query | `string` | no | The search query to use to filter the results. |
| `sort` | query | `list<string>` | no | The way to sort the results. Accepted values: `alphabetical`, `date`, `default`, `duration`, `last_user_action_event_date`. |
| `direction` | query | `list<string>` | no | The sort direction of the results. Accepted values: `asc`, `desc`. |
| `filter_tag` | query | `string` | no | A comma-separated list of tags to filter on. All results must include at least one of these tags. Send multiple values as a string separated by `,`. |
| `filter_tag_all_of` | query | `string` | no | A comma-separated list of tags to filter on. All results must include all of these tags. Send multiple values as a string separated by `,`. |
| `filter_tag_exclude` | query | `string` | no | A comma-separated list of tags to exclude. Send multiple values as a string separated by `,`. |
| `query_fields` | query | `string` | no | A comma-separated list of fields to query over. Send multiple values as a string separated by `,`. |
| `include_subfolders` | query | `boolean` | no | Whether to include subfolders. |
