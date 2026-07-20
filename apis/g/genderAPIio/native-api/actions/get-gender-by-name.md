# Get Gender by Name with GenderAPI.io

Retrieves gender details from GenderAPI.io by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://api.genderapi.io`
- **Official documentation:** [Get Gender by Name](https://www.genderapi.io/docs-gender-from-name-single)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The first name to analyze. |
| `country` | body | `string` | no | Optional ISO 3166-1 alpha-2 country code to improve prediction accuracy. |
| `askToAI` | body | `boolean` | no | Ask GenderAPI's AI model when the name is not found in the database. |
| `forceToGenderize` | body | `boolean` | no | Attempt a gender prediction even for nicknames or non-name words. |
