# Get Organization with e-Gov

Retrieves an organization from e-Gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/organization_show`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [Get Organization](https://data.e-gov.go.jp/data/api/3/action/help_show?name=organization_show)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | query | `string` | yes |
| `include_dataset_count` | query | `boolean` | no |
| `include_tags` | query | `boolean` | no |
| `include_groups` | query | `boolean` | no |
| `include_users` | query | `boolean` | no |
