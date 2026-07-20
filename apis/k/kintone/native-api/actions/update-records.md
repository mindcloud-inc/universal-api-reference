# Update Records with Kintone

Updates existing records in Kintone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/records.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Update Records](https://kintone.dev/en/docs/kintone/rest-api/records/update-records/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | body | `number` | yes | The Kintone app ID. |
| `records` | body | `list<object>` | yes | An array of record update objects. Each item can include id or updateKey, revision, and record. |
| `upsert` | body | `boolean` | no | Create a record when an update target does not already exist. |
