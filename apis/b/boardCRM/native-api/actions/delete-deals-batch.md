# Delete Deals Batch with BoardCRM

Deletes multiple deal records from BoardCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/offer/delete-some`
- **Base URL:** `https://api.boardcrm.io/api`
- **Official documentation:** [Delete Deals Batch](https://dev.boardcrm.io/public/0.1/methods/offer#delete-some)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Deal IDs to delete. |
