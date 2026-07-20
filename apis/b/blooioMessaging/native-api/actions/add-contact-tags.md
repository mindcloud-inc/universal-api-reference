# Add Contact Tags with Blooio Messaging

Adds tags to a contact in Blooio Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/{identifier}/tags`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Add Contact Tags](https://docs.blooio.com/contacts/addContactTags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier. Use an E.164 phone number or email address. |
| `tags` | body | `string` | no | Tags to add to the contact. |
