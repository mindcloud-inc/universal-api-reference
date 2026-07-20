# Add Subscribers with SARE

Creates new subscribers in SARE.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/add`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Add Subscribers](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<object>` | yes | Array of subscriber objects to add through the SARE route. |
