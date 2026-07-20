# Create Application with ironSource

Creates a new application in ironSource.

## Endpoint

- **Method:** `POST`
- **Path:** `partners/publisher/applications/v6`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Create Application](https://docs.unity.com/en-us/grow/levelplay/platform/api/application)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adUnits` | body | `object` | no | Optional ad unit status object, for example {"RewardedVideo":"Live","Interstitial":"Live","OfferWall":"Off","Banner":"Live","NativeAd":"Live"}. |
| `appName` | body | `string` | no | Application name. Required for apps that are not live in the store. |
| `ccpa` | body | `number` | no | Optional CCPA status as an integer: 1 for true, 0 for false. |
| `coppa` | body | `number` | no | COPPA status as an integer: 1 for true, 0 for false. |
| `platform` | body | `string` | no | Operating system for a non-live app: iOS or Android. |
| `storeUrl` | body | `string` | no | Store URL for a live app. |
| `taxonomy` | body | `string` | no | Application sub-genre for a live app. |
