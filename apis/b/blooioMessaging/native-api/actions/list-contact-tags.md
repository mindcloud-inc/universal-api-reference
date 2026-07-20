# List Contact Tags with Blooio Messaging

Retrieves contact tags from Blooio Messaging.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/{identifier}/tags`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [List Contact Tags](https://docs.blooio.com/contacts/listContactTags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier. Use an E.164 phone number or email address. |
