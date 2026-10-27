# Find User with Pipedrive

Find Pipedrive users by their name or email address.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/users/find`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Find User](https://developers.pipedrive.com/docs/api/v1/Persons#getPerson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | no | The term to of the user to search for, either name or email address. |
| `search_by_email` | query | `number` | no | Set to 1 to search users by email instead of name. |
