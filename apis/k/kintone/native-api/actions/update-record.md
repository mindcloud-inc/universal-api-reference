# Update Record with Kintone

Updates an existing record in Kintone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/record.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Update Record](https://kintone.dev/en/docs/kintone/rest-api/records/update-record/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | body | `number` | yes | The Kintone app ID. |
| `id` | body | `number` | yes | The Kintone record ID to update. |
| `record` | body | `object` | yes | The record field updates keyed by Kintone field code. |
| `revision` | body | `number` | no | The expected revision number for optimistic concurrency control. |
