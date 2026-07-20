# Update Status with Kintone

Updates a record status in Kintone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/record/status.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Update Status](https://kintone.dev/en/docs/kintone/rest-api/records/update-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | body | `number` | yes | The Kintone app ID. |
| `id` | body | `number` | yes | The Kintone record ID. |
| `action` | body | `string` | yes | The process management action name to apply. |
| `assignee` | body | `string` | no | Optional user code to assign during the status transition. |
| `revision` | body | `number` | no | The expected record revision number. |
