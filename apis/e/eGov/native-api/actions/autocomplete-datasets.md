# Autocomplete Datasets with e-Gov

Finds datasets in e-Gov by partial name.

## Endpoint

- **Method:** `GET`
- **Path:** `/package_autocomplete`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [Autocomplete Datasets](https://data.e-gov.go.jp/data/api/3/action/help_show?name=package_autocomplete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | query | `string` | yes |
| `limit` | query | `number` | no |
