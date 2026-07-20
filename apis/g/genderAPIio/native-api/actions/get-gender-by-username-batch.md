# Get Gender by Username Batch with GenderAPI.io

Retrieves gender details from GenderAPI.io for multiple usernames.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/username/multi/country`
- **Base URL:** `https://api.genderapi.io`
- **Official documentation:** [Get Gender by Username Batch](https://www.genderapi.io/docs-gender-from-username-multiple)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `list<object>` | yes | Array of username records to analyze. Each object can include username, country, and id. |
