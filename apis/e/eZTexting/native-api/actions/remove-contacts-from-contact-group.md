# Remove Contacts from Contact Group with EZ Texting

Removes contacts from a contact group in EZ Texting.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contact-groups/:id/contacts`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [Remove Contacts from Contact Group](https://developers.eztexting.com/reference/contactsremove-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact group ID |
| `phoneNumbers[]` | query | `array<string>` | yes | Phone numbers to remove |
