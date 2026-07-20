# List Projects with Vimeo

Retrieves a user's projects from Vimeo.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id/projects`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List Projects](https://developer.vimeo.com/api/reference/folders#get_projects)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user. |
| `query` | query | `string` | no | The search query to use to filter the results. |
| `sort` | query | `list<string>` | no | The way to sort the results. Accepted values: `date`, `default`, `modified_time`, `name`, `pinned_on`. |
| `direction` | query | `list<string>` | no | The sort direction of the results. Accepted values: `asc`, `desc`. |
