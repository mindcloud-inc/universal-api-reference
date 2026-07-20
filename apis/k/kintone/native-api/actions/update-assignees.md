# Update Assignees with Kintone

Updates record assignees in Kintone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/record/assignees.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Update Assignees](https://kintone.dev/en/docs/kintone/rest-api/records/update-assignees/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | body | `number` | yes | The Kintone app ID. |
| `id` | body | `number` | yes | The Kintone record ID. |
| `assignees[]` | body | `array<string>` | yes | The user codes that should remain assigned to the record. |
| `revision` | body | `number` | no | The expected record revision number. |
