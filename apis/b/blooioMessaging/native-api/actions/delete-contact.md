# Delete Contact with Blooio Messaging

Deletes a contact from Blooio Messaging.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/{identifier}`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Delete Contact](https://docs.blooio.com/contacts/deleteContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier. Use an E.164 phone number or email address. |
