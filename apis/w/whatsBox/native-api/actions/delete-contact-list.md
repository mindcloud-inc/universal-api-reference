# Delete Contact List with WhatsBox

Deletes an existing contact list from WhatsBox.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contact-lists/:id`
- **Base URL:** `https://api.whatsbox.io`
- **Official documentation:** [Delete Contact List](https://api.whatsbox.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Contact list ID. |
| `delete_contacts` | query | `boolean` | no | Delete contacts along with the list. |
