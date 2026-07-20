# Get Gender by Name (GET) with GenderAPI.io

Retrieves gender details from GenderAPI.io by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/api`
- **Base URL:** `https://api.genderapi.io`
- **Official documentation:** [Get Gender by Name (GET)](https://www.genderapi.io/docs-gender-from-name-single)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | query | `string` | yes |
| `country` | query | `string` | no |
| `askToAI` | query | `boolean` | no |
| `forceToGenderize` | query | `boolean` | no |
