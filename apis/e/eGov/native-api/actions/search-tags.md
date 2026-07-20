# Search Tags with e-Gov

Finds tags in e-Gov by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/tag_search`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [Search Tags](https://data.e-gov.go.jp/data/api/3/action/help_show?name=tag_search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | query | `string` | yes |
| `vocabulary_id` | query | `string` | no |
