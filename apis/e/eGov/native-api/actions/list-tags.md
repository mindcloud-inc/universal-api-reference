# List Tags with e-Gov

Retrieves tags from e-Gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/tag_list`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [List Tags](https://data.e-gov.go.jp/data/api/3/action/help_show?name=tag_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Return tags whose names contain this text. |
| `vocabulary_id` | query | `string` | no | — |
| `all_fields` | query | `boolean` | no | Return full tag records instead of names. |
