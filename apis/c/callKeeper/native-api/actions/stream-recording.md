# Stream Recording with CallKeeper

Retrieves a recording stream from CallKeeper.

## Endpoint

- **Method:** `GET`
- **Path:** `/recordings/:recording_id/stream`
- **Base URL:** `https://api.callkeeper.ai`
- **Official documentation:** [Stream Recording](https://api.callkeeper.ai/docs#/Recordings/stream_recording_recordings__recording_id__stream_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recording_id` | path | `string` | yes | Recording identifier. |
