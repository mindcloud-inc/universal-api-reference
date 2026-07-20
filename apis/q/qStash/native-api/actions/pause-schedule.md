# Pause Schedule with QStash

Pauses an existing schedule in QStash.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/schedules/:scheduleId/pause`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Pause Schedule](https://upstash.com/docs/qstash/api-refence/schedules/pause-a-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scheduleId` | path | `string` | yes | Identifier of the schedule to pause. |
