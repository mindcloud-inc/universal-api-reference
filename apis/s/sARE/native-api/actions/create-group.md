# Create Group with SARE

Creates a new group in SARE.

## Endpoint

- **Method:** `POST`
- **Path:** `/group/add`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Create Group](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groups[]` | body | `array<object>` | yes | Array of group objects to send to the SARE create-group route. |
