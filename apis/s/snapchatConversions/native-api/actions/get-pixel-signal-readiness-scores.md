# Get Pixel Signal Readiness Scores with Snapchat Conversions

Retrieves pixel signal readiness scores in Snapchat Conversions.

## Endpoint

- **Method:** `GET`
- **Path:** `/pixels/:pixelId/event_quality_scores`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Get Pixel Signal Readiness Scores](https://developers.snap.com/api/marketing-api/Ads-API/signal-readiness-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pixelId` | path | `string` | yes | The Snapchat Pixel ID to retrieve event quality scores for. |
| `locale` | query | `string` | no | Optional locale code for the response. |
