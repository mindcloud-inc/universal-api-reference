# Trigger Messaging Event By Mobile And Email with Authkey

Triggers a messaging event by mobile and email in Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Trigger Messaging Event By Mobile And Email](https://authkey.io/voice-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Recipient country dialing code. |
| `eid` | query | `string` | no | Authkey event ID. |
| `email` | query | `string` | no | Recipient email address. |
| `mobile` | query | `string` | no | Recipient mobile number. |
