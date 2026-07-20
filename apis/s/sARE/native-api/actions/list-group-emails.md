# List Group Emails with SARE

Retrieves subscriber email addresses from a SARE group.

## Endpoint

- **Method:** `GET`
- **Path:** `/group/emails/:group/:page`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [List Group Emails](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `number` | yes | Group identifier from the SARE account. |
| `page` | path | `number` | yes | Zero-based page number for the SARE route. |
