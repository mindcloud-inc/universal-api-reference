# Update Contact List with Magileads

Updates an existing contact list in Magileads.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact-lists/:contact_list_id`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Update Contact List](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_list_id` | path | `number` | yes | The contact list ID. |
| `name` | body | `string` | no | The updated contact list name. |
