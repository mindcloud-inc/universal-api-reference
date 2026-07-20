# Add Record with Kintone

Creates a record in Kintone.

## Endpoint

- **Method:** `POST`
- **Path:** `/record.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Add Record](https://kintone.dev/en/docs/kintone/rest-api/records/add-record/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | body | `number` | yes | The Kintone app ID. |
| `record` | body | `object` | yes | The record payload keyed by Kintone field code. |
