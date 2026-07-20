# Trigger Messaging Event By Mobile with Authkey

Triggers a messaging event for a mobile number in Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Trigger Messaging Event By Mobile](https://authkey.io/sms-api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Recipient country dialing code. |
| `eid` | query | `string` | no | Authkey event ID. |
| `mobile` | query | `string` | no | Recipient mobile number. |
