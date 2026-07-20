# Check Contact Capabilities with Blooio Messaging

Retrieves contact capabilities from Blooio Messaging.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/{identifier}/capabilities`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Check Contact Capabilities](https://docs.blooio.com/contacts/getContactCapabilities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier. Use an E.164 phone number or email address. |
