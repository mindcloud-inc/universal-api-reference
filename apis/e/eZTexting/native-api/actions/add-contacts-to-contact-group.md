# Add Contacts to Contact Group with EZ Texting

Adds contacts to a contact group in EZ Texting.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact-groups/:id/contacts`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [Add Contacts to Contact Group](https://developers.eztexting.com/reference/contactsadd-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact group ID |
| `phoneNumbers[]` | query | `array<string>` | yes | Phone numbers to add |
