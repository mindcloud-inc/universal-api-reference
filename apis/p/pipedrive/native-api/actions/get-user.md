# Get User with Pipedrive

Retrieves a person from Pipedrive.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/users/:id`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Get User](https://developers.pipedrive.com/docs/api/v1/Persons#getPerson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique ID of the user. |
| `include_fields` | query | `string` | no | Comma-separated additional fields to include. |
| `custom_fields` | query | `string` | no | Comma-separated custom field keys to include. |
