# Get Subscribers By Email List with SARE

Retrieves subscribers from SARE by email address list.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/by_email_list/:page`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Get Subscribers By Email List](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<object>` | yes | Array of email lookup objects for the SARE route. |
| `page` | path | `number` | yes | Zero-based page number for the SARE route. |
