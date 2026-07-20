# Remove Contact Tag with Blooio Messaging

Removes a tag from a contact in Blooio Messaging.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/{identifier}/tags/{tag}`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Remove Contact Tag](https://docs.blooio.com/contacts/removeContactTag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier. Use an E.164 phone number or email address. |
| `tag` | path | `string` | yes | Tag value to remove from the contact. |
