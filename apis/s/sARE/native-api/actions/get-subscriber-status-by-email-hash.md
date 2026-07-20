# Get Subscriber Status By Email Hash with SARE

Retrieves subscriber status from SARE by email hash.

## Endpoint

- **Method:** `GET`
- **Path:** `/email/status_hash/:emailHash`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Get Subscriber Status By Email Hash](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailHash` | path | `string` | yes | MD5 hash for the subscriber email, derived from the SARE account salt and email value. |
