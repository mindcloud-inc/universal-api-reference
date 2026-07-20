# Get Gender by Email (GET) with GenderAPI.io

Retrieves gender details from GenderAPI.io by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/email`
- **Base URL:** `https://api.genderapi.io`
- **Official documentation:** [Get Gender by Email (GET)](https://www.genderapi.io/docs-gender-from-email-single)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | query | `string` | yes |
| `country` | query | `string` | no |
| `askToAI` | query | `boolean` | no |
