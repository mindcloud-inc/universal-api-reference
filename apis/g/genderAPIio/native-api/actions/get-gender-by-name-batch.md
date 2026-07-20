# Get Gender by Name Batch with GenderAPI.io

Retrieves gender details from GenderAPI.io for multiple names.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/name/multi/country`
- **Base URL:** `https://api.genderapi.io`
- **Official documentation:** [Get Gender by Name Batch](https://www.genderapi.io/docs-gender-from-name-multiple)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `list<object>` | yes | Array of name records to analyze. Each object can include name, country, and id. |
