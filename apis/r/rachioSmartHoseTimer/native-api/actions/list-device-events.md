# List Device Events with Rachio Smart Hose Timer

Retrieves device event records from Rachio.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/device/:id/event`
- **Base URL:** `https://api.rach.io/1`
- **Official documentation:** [List Device Events](https://rachio.readme.io/reference/publicdeviceideventstarttimestarttimeendtimeendtim)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endTime` | query | `number` | yes | Query end time in Unix epoch milliseconds. |
| `id` | path | `string` | yes | Controller device UUID. |
| `startTime` | query | `number` | yes | Query start time in Unix epoch milliseconds. |
