# Trigger Email Event with Authkey

Triggers an email event in Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Trigger Email Event](https://authkey.io/email-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Recipient email address. |
| `msisdn` | query | `string` | yes | Recipient mobile number used by the event. |
| `country_code` | query | `string` | yes | Recipient country dialing code. |
| `eid` | query | `string` | yes | Authkey event ID. |
