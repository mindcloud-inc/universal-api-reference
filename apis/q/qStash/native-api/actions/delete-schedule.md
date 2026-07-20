# Delete Schedule with QStash

Deletes an existing schedule from QStash.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/schedules/:scheduleId`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Delete Schedule](https://upstash.com/docs/qstash/api-refence/schedules/delete-a-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scheduleId` | path | `string` | yes | Identifier of the schedule to delete. |
