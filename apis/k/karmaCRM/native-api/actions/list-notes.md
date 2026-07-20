# List Notes with Karma CRM

Retrieves note histories from Karma CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/histories.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [List Notes](https://docs.karmacrm.com/#get-all-notes-histories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[external_type]` | query | `string` | no | Optional history external type, such as Note. |
| `filters[history_record_id]` | query | `string` | no | Optional associated record ID. |
| `filters[history_record_type]` | query | `string` | no | Optional associated record type, such as Contact or Company. |
| `page` | query | `number` | no | Page number for note histories. |
