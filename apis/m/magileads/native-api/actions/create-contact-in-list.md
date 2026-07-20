# Create Contact In List with Magileads

Imports a contact into a Magileads contact list.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact-lists/:contact_list_id/contact`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Create Contact In List](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_list_id` | path | `number` | yes | The contact list ID. |
| `properties[]` | body | `array<object>` | yes | The contact properties to import. |
