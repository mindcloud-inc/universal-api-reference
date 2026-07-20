# Get Recording with Avoma

Retrieves a recording for a meeting from Avoma.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/recordings/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [Get Recording](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_uuid` | query | `string` | yes | Unique ID of the meeting. |
