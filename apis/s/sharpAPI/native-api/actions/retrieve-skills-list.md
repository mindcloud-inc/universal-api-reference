# Retrieve Skills List with SharpAPI

Retrieves skills from SharpAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/utilities/skills_list`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Retrieve Skills List](https://sharpapi.com/en/catalog/utility/skills-database-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_related` | query | `boolean` | no | Include related skills with relevancy weights. |
| `name` | query | `string` | no | Filter skills by name with a partial match. |
