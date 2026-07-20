# Autocomplete Formats with e-Gov

Finds resource formats in e-Gov by partial name.

## Endpoint

- **Method:** `GET`
- **Path:** `/format_autocomplete`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [Autocomplete Formats](https://data.e-gov.go.jp/data/api/3/action/help_show?name=format_autocomplete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | query | `string` | yes |
| `limit` | query | `number` | no |
