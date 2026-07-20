# List Records with Kintone

Retrieves records from Kintone.

## Endpoint

- **Method:** `GET`
- **Path:** `/records.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [List Records](https://kintone.dev/en/docs/kintone/rest-api/records/get-records/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | query | `number` | yes | The Kintone app ID. |
| `query` | query | `string` | no | A Kintone query expression used to filter and sort records. |
| `totalCount` | query | `boolean` | no | Return the total count of matching records in addition to the record list. |
