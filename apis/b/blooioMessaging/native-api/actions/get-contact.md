# Get Contact with Blooio Messaging

Retrieves a contact from Blooio Messaging.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/{identifier}`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Get Contact](https://docs.blooio.com/contacts/getContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier. Use an E.164 phone number or email address. |
