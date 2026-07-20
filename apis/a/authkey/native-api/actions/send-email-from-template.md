# Send Email From Template with Authkey

Sends a templated email through Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send Email From Template](https://authkey.io/email-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Recipient email address. |
| `mid` | query | `string` | yes | Email template ID. |
