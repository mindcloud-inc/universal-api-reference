# Resume Schedule with QStash

Resumes a paused schedule in QStash.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/schedules/:scheduleId/resume`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Resume Schedule](https://upstash.com/docs/qstash/api-refence/schedules/resume-a-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scheduleId` | path | `string` | yes | Identifier of the schedule to resume. |
