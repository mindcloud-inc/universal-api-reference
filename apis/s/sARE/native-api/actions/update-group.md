# Update Group with SARE

Updates an existing group in SARE.

## Endpoint

- **Method:** `POST`
- **Path:** `/group/edit`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Update Group](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groups[]` | body | `array<object>` | yes | Array of group objects to send to the SARE update-group route. |
