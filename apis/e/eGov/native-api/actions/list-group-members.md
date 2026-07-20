# List Group Members with e-Gov

Retrieves group members from e-Gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/member_list`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [List Group Members](https://data.e-gov.go.jp/data/api/3/action/help_show?name=member_list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | query | `string` | yes |
| `object_type` | query | `string` | no |
| `capacity` | query | `string` | no |
