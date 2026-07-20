# Get Meeting Insights with Avoma

Retrieves insights for a completed meeting from Avoma.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meetings/:meetingUuid/insights/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [Get Meeting Insights](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_uuid` | path | `string` | yes | Unique ID of the meeting. |
