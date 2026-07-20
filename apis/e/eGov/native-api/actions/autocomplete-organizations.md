# Autocomplete Organizations with e-Gov

Finds organizations in e-Gov by partial name.

## Endpoint

- **Method:** `GET`
- **Path:** `/organization_autocomplete`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [Autocomplete Organizations](https://data.e-gov.go.jp/data/api/3/action/help_show?name=organization_autocomplete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | query | `string` | yes |
| `limit` | query | `number` | no |
