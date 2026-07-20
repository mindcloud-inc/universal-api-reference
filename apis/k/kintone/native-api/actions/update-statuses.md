# Update Statuses with Kintone

Updates record statuses in Kintone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/records/status.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Update Statuses](https://kintone.dev/en/docs/kintone/rest-api/records/update-statuses/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | body | `number` | yes | The Kintone app ID. |
| `records` | body | `list<object>` | yes | An array of status update objects. Each item can include id, action, assignee, and revision. |
