# Get Gender by Email with GenderAPI.io

Retrieves gender details from GenderAPI.io by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/email`
- **Base URL:** `https://api.genderapi.io`
- **Official documentation:** [Get Gender by Email](https://www.genderapi.io/docs-gender-from-email-single)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to analyze. |
| `country` | body | `string` | no | Optional ISO 3166-1 alpha-2 country code to improve prediction accuracy. |
| `askToAI` | body | `boolean` | no | Ask GenderAPI's AI model when the name extracted from the email is not found in the database. |
