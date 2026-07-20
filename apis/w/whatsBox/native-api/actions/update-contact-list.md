# Update Contact List with WhatsBox

Updates an existing contact list in WhatsBox.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact-lists/:id`
- **Base URL:** `https://api.whatsbox.io`
- **Official documentation:** [Update Contact List](https://api.whatsbox.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Contact list ID. |
| `name` | body | `string` | yes | Updated contact list name. |
