# Get Schedule with QStash

Retrieves a schedule from QStash by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/schedules/:scheduleId`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Get Schedule](https://upstash.com/docs/qstash/api-refence/schedules/get-a-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scheduleId` | path | `string` | yes | Identifier of the schedule to retrieve. |
