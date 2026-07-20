# Create Schedule with QStash

Creates a recurring delivery schedule in QStash.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/schedules/:destination`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Create Schedule](https://upstash.com/docs/qstash/api-refence/schedules/create-a-schedule)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination` | path | `string` | yes | Destination URL or URL Group name. |
| `Upstash-Cron` | body | `string` | yes | Cron expression for the schedule. |
