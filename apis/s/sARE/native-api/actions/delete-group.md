# Delete Group with SARE

Deletes an existing group from SARE.

## Endpoint

- **Method:** `POST`
- **Path:** `/group/remove/:group`
- **Base URL:** `https://s.enewsletter.pl/api/v1/{uid}`
- **Official documentation:** [Delete Group](https://dev.sare.pl/rest-api/other/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `number` | yes | Group identifier to delete. |
