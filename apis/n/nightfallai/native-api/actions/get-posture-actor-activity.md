# Get Posture Actor Activity with Nightfall.ai

Retrieves activity for a posture actor from Nightfall.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/posture/v1/actor/activity`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Get Posture Actor Activity](https://help.nightfall.ai/developer-api/nightfall_apis/posture-management-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actorID` | query | `string` | yes | The actor UUID whose posture activity you want to fetch. |
| `rangeStart` | query | `number` | yes | Required Unix timestamp in seconds for the start of the activity window. |
| `rangeEnd` | query | `number` | yes | Required Unix timestamp in seconds for the end of the activity window. |
