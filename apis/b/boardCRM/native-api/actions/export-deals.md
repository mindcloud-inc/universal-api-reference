# Export Deals with BoardCRM

Exports deal records from the BoardCRM workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/offer/export`
- **Base URL:** `https://api.boardcrm.io/api`
- **Official documentation:** [Export Deals](https://dev.boardcrm.io/public/0.1/methods/offer#export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_column` | body | `string` | no | Date field to filter exported deals by. |
| `date_from` | body | `string` | no | Start datetime for the export window. |
| `date_to` | body | `string` | no | End datetime for the export window. |
