# List Contacts with Emailchef

Retrieves a list of contacts from Emailchef.

## Endpoint

- **Method:** `GET`
- **Path:** `contacts`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [List Contacts](https://emailchef.com/integration/#/Contacts/getContacts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional contact status filter. |
| `list_id` | query | `string` | no | Optional list ID to narrow the contact list. |
