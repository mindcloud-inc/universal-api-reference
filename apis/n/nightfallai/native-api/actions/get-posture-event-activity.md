# Get Posture Event Activity with Nightfall.ai

Retrieves activity for a posture event from Nightfall.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/posture/v1/events/:eventId/activity`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Get Posture Event Activity](https://help.nightfall.ai/developer-api/nightfall_apis/posture-management-apis)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The UUID of the posture event whose activity you want to fetch. |
