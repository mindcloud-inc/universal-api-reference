# Create Contact with Blooio Messaging

Creates a new contact in Blooio Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Create Contact](https://docs.blooio.com/contacts/createContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | — |
| `identifier` | body | `string` | yes | Contact identifier. Use an E.164 phone number or email address. |
| `last_name` | body | `string` | no | — |
