# Make Phone Call with PushCallMe

Creates a new phone call in PushCallMe.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/call`
- **Base URL:** `https://pushcall.me`
- **Official documentation:** [Make Phone Call](https://pushcall.me/docs/phone-call-via-http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Caller selector. PushCall's docs describe this as a caller ID index, while provided webhook examples may use a full caller number. |
| `to` | query | `string<string>` | yes | Destination phone number to call. PushCall's docs also mention repeating the `to` query parameter for multiple recipients, but this draft currently keeps the single-recipient contract until repeated query values can be modeled cleanly in runtime. |
