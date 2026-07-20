# Get Posture Event with Nightfall.ai

Retrieves a posture event from Nightfall.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/posture/v1/events/:eventId`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Get Posture Event](https://help.nightfall.ai/developer-api/nightfall_apis/posture-management-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The UUID of the posture event to fetch. |
