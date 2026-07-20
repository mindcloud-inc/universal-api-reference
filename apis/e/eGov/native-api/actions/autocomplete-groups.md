# Autocomplete Groups with e-Gov

Finds groups in e-Gov by partial name.

## Endpoint

- **Method:** `GET`
- **Path:** `/group_autocomplete`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [Autocomplete Groups](https://data.e-gov.go.jp/data/api/3/action/help_show?name=group_autocomplete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | query | `string` | yes |
| `limit` | query | `number` | no |
