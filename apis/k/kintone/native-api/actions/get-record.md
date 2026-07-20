# Get Record with Kintone

Retrieves a record from Kintone.

## Endpoint

- **Method:** `GET`
- **Path:** `/record.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Get Record](https://kintone.dev/en/docs/kintone/rest-api/records/get-record/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | query | `number` | yes | The Kintone app ID. |
| `id` | query | `number` | yes | The Kintone record ID. |
