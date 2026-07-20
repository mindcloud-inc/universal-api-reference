# Find Companies with profileAPI

Finds companies in profileAPI by filter criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/find`
- **Base URL:** `https://api.profileapi.com/2024-03-01`
- **Official documentation:** [Find Companies](https://documentation.profileapi.com/api-reference/find-companies/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | Filter groups containing all/any filter arrays. |
| `limit` | body | `number` | no | Maximum number of companies to return. Official docs list default 10 and maximum 1000 for company search. |
