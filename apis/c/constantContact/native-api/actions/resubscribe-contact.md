# Resubscribe Contact with Constant Contact

Resubscribes a contact in Constant Contact.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/resubscribe/:contact_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Resubscribe Contact](https://developer.constantcontact.com/api_guide/contacts_re-subscribe.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Unique ID of the contact to resubscribe. |
| `list_ids[]` | body | `array<string>` | yes | List IDs to resubscribe the contact to (array of strings). |
