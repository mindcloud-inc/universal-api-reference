# Delete Subscribers with SARE

Deletes subscribers from SARE.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/delete`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Delete Subscribers](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | yes | Array of subscriber email addresses to delete. |
