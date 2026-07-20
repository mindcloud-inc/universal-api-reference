# Delete Records with Kintone

Deletes existing records from Kintone.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/records.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Delete Records](https://kintone.dev/en/docs/kintone/rest-api/records/delete-records/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | body | `number` | yes | The Kintone app ID. |
| `ids[]` | body | `array<number>` | yes | The record IDs to delete. |
| `revisions[]` | body | `array<number>` | no | Optional revision numbers that must match before deletion succeeds. |
