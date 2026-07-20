# Create Datalist Entry Items with Global Patron

Adds datalist entry items to Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/restricted/datalist/{datalistId}/entry`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Create Datalist Entry Items](https://www.globalpatron.com/developers/api/datalists/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datalistId` | path | `string` | yes | ID of the datalist. |
| `entry_items[]` | body | `array<object>` | yes | Array of datalist entry items to create. |
