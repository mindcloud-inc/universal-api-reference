# Stop Tracking with EARLY

Stops the current tracking session in EARLY.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/tracking/stop`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Stop Tracking](https://developers.early.app/#b5f602d3-cc31-4a03-abd9-9fa397121ab5)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stoppedAt` | body | `string` | no | Optional tracking stop timestamp in EARLY format, for example 2016-02-03T05:00:00.000. |
