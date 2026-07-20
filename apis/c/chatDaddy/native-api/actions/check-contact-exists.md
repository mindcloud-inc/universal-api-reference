# Check Contact Exists with ChatDaddy

Checks whether a contact exists in ChatDaddy.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/exists`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Check Contact Exists](https://chatdaddy.stoplight.io/docs/openapi/1b1833007efdf-check-a-given-user-exists-on-the-im-platform)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | yes | Platform type to check, for example a WhatsApp user lookup. |
