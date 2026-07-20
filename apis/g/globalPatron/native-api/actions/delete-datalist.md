# Delete Datalist with Global Patron

Deletes a datalist from Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/restricted/datalist/{datalistId}?for_deletion=1`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Delete Datalist](https://www.globalpatron.com/developers/api/datalists/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datalistId` | path | `string` | yes | ID of the datalist to delete. |
