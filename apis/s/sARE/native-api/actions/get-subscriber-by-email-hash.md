# Get Subscriber By Email Hash with SARE

Retrieves a subscriber from SARE by email hash.

## Endpoint

- **Method:** `GET`
- **Path:** `/email/by_email_hash/:emailHash`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Get Subscriber By Email Hash](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailHash` | path | `string` | yes | MD5 hash for the subscriber email, derived from the SARE account salt and email value. |
