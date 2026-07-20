# Clear Group with SARE

Removes all email addresses from a SARE group.

## Endpoint

- **Method:** `POST`
- **Path:** `/group/clear/:group`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Clear Group](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `number` | yes | Group identifier to clear. |
