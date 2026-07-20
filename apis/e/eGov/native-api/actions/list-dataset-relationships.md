# List Dataset Relationships with e-Gov

Retrieves a dataset's relationships from e-Gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/package_relationships_list`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [List Dataset Relationships](https://data.e-gov.go.jp/data/api/3/action/help_show?name=package_relationships_list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | query | `string` | yes |
| `id2` | query | `string` | no |
| `rel` | query | `string` | no |
