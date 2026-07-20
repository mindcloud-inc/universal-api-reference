# Find Committee Names with OpenFEC

Finds committee names in OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/names/committees/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [Find Committee Names](https://api.open.fec.gov/developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Committee name search text. |
