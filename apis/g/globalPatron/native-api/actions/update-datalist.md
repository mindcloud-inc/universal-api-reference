# Update Datalist with Global Patron

Updates a datalist in Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/restricted/datalist/{datalistId}`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Update Datalist](https://www.globalpatron.com/developers/api/datalists/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datalistId` | path | `string` | yes | ID of the datalist. |
