# Get Exfiltration Event with Nightfall.ai

Retrieves an exfiltration event from Nightfall.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/exfiltration/v1/events/:eventId`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Get Exfiltration Event](https://help.nightfall.ai/developer-api/nightfall_apis/exfiltration-prevention-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The UUID of the exfiltration event to fetch. |
