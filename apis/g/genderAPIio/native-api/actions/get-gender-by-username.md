# Get Gender by Username with GenderAPI.io

Retrieves gender details from GenderAPI.io by username.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/username`
- **Base URL:** `https://api.genderapi.io`
- **Official documentation:** [Get Gender by Username](https://www.genderapi.io/docs-gender-from-username-single)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | The username or nickname to analyze. |
| `country` | body | `string` | no | Optional ISO 3166-1 alpha-2 country code to improve prediction accuracy. |
| `askToAI` | body | `boolean` | no | Ask GenderAPI's AI model when the username cannot be matched from the database. |
| `forceToGenderize` | body | `boolean` | no | Attempt a gender prediction even for nicknames or non-name words. |
