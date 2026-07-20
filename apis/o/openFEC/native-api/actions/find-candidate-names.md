# Find Candidate Names with OpenFEC

Finds candidate names in OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/names/candidates/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [Find Candidate Names](https://api.open.fec.gov/developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Candidate name search text. |
