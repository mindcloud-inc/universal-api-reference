# Get App Signal Readiness Scores with Snapchat Conversions

Retrieves app signal readiness scores in Snapchat Conversions.

## Endpoint

- **Method:** `GET`
- **Path:** `/mobile_apps/:snapAppId/event_quality_scores`
- **Base URL:** `https://adsapi.snapchat.com/v1`
- **Official documentation:** [Get App Signal Readiness Scores](https://developers.snap.com/api/marketing-api/Ads-API/signal-readiness-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `snapAppId` | path | `string` | yes | The Snapchat mobile app ID to retrieve event quality scores for. |
| `locale` | query | `string` | no | Optional locale code for the response. |
