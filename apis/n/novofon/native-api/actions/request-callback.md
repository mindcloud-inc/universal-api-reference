# Request Callback with Novofon

Creates a callback request in Novofon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/request/callback/`
- **Base URL:** `https://api.novofon.com`
- **Official documentation:** [Request Callback](https://novofon.com/instructions/api/#callback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Your phone number, SIP, or PBX internal number that receives the callback. |
| `predicted` | query | `string` | no | Optional provider flag for predictive callback behavior. Pass the provider-accepted truthy value when needed. |
| `sip` | query | `string` | no | Optional SIP user number or PBX internal number used to place the call. |
| `to` | query | `string` | yes | Phone number or SIP destination to call. |
