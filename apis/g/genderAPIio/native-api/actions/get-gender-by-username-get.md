# Get Gender by Username (GET) with GenderAPI.io

Retrieves gender details from GenderAPI.io by username.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/username`
- **Base URL:** `https://api.genderapi.io`
- **Official documentation:** [Get Gender by Username (GET)](https://www.genderapi.io/docs-gender-from-username-single)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `username` | query | `string` | yes |
| `country` | query | `string` | no |
| `askToAI` | query | `boolean` | no |
| `forceToGenderize` | query | `boolean` | no |
