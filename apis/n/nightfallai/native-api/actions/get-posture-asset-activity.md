# Get Posture Asset Activity with Nightfall.ai

Retrieves activity for a posture asset from Nightfall.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/posture/v1/asset/activity`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Get Posture Asset Activity](https://help.nightfall.ai/developer-api/nightfall_apis/posture-management-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assetID` | query | `string` | yes | The asset UUID whose posture activity you want to fetch. |
| `rangeStart` | query | `number` | yes | Required Unix timestamp in seconds for the start of the activity window. |
| `rangeEnd` | query | `number` | yes | Required Unix timestamp in seconds for the end of the activity window. |
