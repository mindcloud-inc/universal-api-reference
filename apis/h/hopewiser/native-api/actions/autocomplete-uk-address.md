# Autocomplete UK Address with Hopewiser

## Endpoint

- **Method:** `GET`
- **Path:** `/autoc/json/:maf`
- **Base URL:** `https://cloud.hopewiser.com`
- **Official documentation:** [Autocomplete UK Address](https://www.hopewiser.com/developer-document/autocomplete-rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `maf` | path | `string` | yes | Hopewiser MAF identity. This tenant is provisioned for uk-rm-paf-mr. |
| `q` | query | `string` | yes | Autocomplete address search text. |
