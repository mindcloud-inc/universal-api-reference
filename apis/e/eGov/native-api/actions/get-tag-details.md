# Get Tag Details with e-Gov

Retrieves a tag and its datasets from e-Gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/tag_show`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [Get Tag Details](https://data.e-gov.go.jp/data/api/3/action/help_show?name=tag_show)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | query | `string` | yes |
| `vocabulary_id` | query | `string` | no |
