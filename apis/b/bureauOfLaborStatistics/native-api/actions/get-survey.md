# Get Survey with Bureau of Labor Statistics

Retrieves metadata for a Bureau of Labor Statistics survey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/:surveyAbbreviation`
- **Base URL:** `https://api.bls.gov/publicAPI/v2`
- **Official documentation:** [Get Survey](https://www.bls.gov/developers/api_signature_v2.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyAbbreviation` | path | `string` | yes | BLS survey abbreviation, for example TU. |
