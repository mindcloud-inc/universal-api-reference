# Change Deal Column with BoardCRM

Moves deals between columns in BoardCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/offer/change-column`
- **Base URL:** `https://api.boardcrm.io/api`
- **Official documentation:** [Change Deal Column](https://dev.boardcrm.io/public/0.1/methods/offer#change-column)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `column_id_from` | body | `number` | yes | Current deal column ID. |
| `column_id_to` | body | `number` | yes | Destination deal column ID. |
| `ids[]` | body | `array<number>` | yes | Deal IDs to move to the destination column. |
