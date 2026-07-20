# Guest Reveal Secret with One-Time Secret

Reveals and consumes a guest secret from One-Time Secret by identifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/guest/secret/:identifier/reveal`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [Guest Reveal Secret](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_guest_revealsecret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Secret identifier to reveal. |
