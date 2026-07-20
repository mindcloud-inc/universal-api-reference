# Get Contact with Selzy

Retrieves a contact from Selzy.

## Endpoint

- **Method:** `POST`
- **Path:** `getContact`
- **Base URL:** `https://api.selzy.com/en/api`
- **Official documentation:** [Get Contact](https://selzy.com/en/support/api/contacts/getcontact/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address of the contact to retrieve. |
| `include_lists` | query | `number` | no | Set to 1 to include contact list memberships. |
| `include_fields` | query | `number` | no | Set to 1 to include custom contact fields. |
| `include_details` | query | `number` | no | Set to 1 to include detailed activity metadata. |
