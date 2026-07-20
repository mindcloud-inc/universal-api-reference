# Get Group with e-Gov

Retrieves a group from e-Gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/group_show`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [Get Group](https://data.e-gov.go.jp/data/api/3/action/help_show?name=group_show)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | query | `string` | yes |
| `include_dataset_count` | query | `boolean` | no |
| `include_tags` | query | `boolean` | no |
| `include_groups` | query | `boolean` | no |
| `include_users` | query | `boolean` | no |
