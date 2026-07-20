# Get Contact Count with Selzy

Retrieves the contact count for a Selzy list.

## Endpoint

- **Method:** `POST`
- **Path:** `getContactCount`
- **Base URL:** `https://api.selzy.com/en/api`
- **Official documentation:** [Get Contact Count](https://selzy.com/en/support/api/contacts/getcontactcount/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | query | `number` | yes | List code to search within. |
| `params[type]` | query | `string` | no | Search contact type: address or phone. |
| `params[search]` | query | `string` | no | Substring to search within email or phone values. |
| `params[tagId]` | query | `number` | no | Filter by a specific tag ID. |
