# Find Persons with profileAPI

Finds persons in profileAPI by filter criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/persons/find`
- **Base URL:** `https://api.profileapi.com/2024-03-01`
- **Official documentation:** [Find Persons](https://documentation.profileapi.com/api-reference/find-persons/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | Filter groups containing all/any filter arrays. |
| `limit` | body | `number` | no | Maximum number of persons to return. Official docs list default 10 and maximum 100. |
