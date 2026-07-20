# Update Subscribers with SARE

Updates existing subscribers in SARE.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/edit`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Update Subscribers](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<object>` | yes | Array of subscriber objects to update through the SARE route. |
