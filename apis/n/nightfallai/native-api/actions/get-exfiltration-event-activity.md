# Get Exfiltration Event Activity with Nightfall.ai

Retrieves activity for an exfiltration event from Nightfall.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/exfiltration/v1/events/:eventId/activity`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Get Exfiltration Event Activity](https://help.nightfall.ai/developer-api/nightfall_apis/exfiltration-prevention-apis)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The UUID of the exfiltration event whose activity you want to fetch. |
