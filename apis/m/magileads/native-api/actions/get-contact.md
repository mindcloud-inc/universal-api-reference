# Get Contact with Magileads

Retrieves a contact profile from a Magileads contact list.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact-lists/:contact_list_id/contacts/:contact_id`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Get Contact](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_list_id` | path | `number` | yes | The contact list ID. |
| `contact_id` | path | `number` | yes | The contact ID. |
