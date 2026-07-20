# Verify Email with Emailable

Verifies an email address in Emailable.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/verify`
- **Base URL:** `https://api.emailable.com`
- **Official documentation:** [Verify Email](https://emailable.com/docs/api/#verify-an-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The email address you want Emailable to verify. |
| `smtp` | query | `boolean` | no | Set to false to skip the SMTP step and get a faster, less accurate response. |
| `accept_all` | query | `boolean` | no | Set to true to perform an accept-all mailbox check. |
| `timeout` | query | `number` | no | How many seconds to wait before Emailable returns a 249 retry-later response. Minimum 2, maximum 10. |
