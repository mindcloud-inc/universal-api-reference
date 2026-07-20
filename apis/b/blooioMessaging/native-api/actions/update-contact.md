# Update Contact with Blooio Messaging

Updates an existing contact in Blooio Messaging.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/{identifier}`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Update Contact](https://docs.blooio.com/contacts/updateContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | — |
| `identifier` | path | `string` | yes | Contact identifier. Use an E.164 phone number or email address. |
| `last_name` | body | `string` | no | — |
