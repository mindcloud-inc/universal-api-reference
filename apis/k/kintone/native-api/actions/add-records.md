# Add Records with Kintone

Creates records in Kintone.

## Endpoint

- **Method:** `POST`
- **Path:** `/records.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Add Records](https://kintone.dev/en/docs/kintone/rest-api/records/add-records/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | body | `number` | yes | The Kintone app ID. |
| `records` | body | `list<object>` | yes | An array of record payloads keyed by Kintone field code. |
