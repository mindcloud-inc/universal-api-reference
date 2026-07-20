# Get Video Views with Vooplayer

Retrieves video view records from Vooplayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/views/getViews`
- **Base URL:** `https://api.spotlightr.com`
- **Official documentation:** [Get Video Views](https://app.spotlightr.com/docs/api/#getViews)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoID` | query | `number` | yes | Video metrics ID. |
| `customViewerID` | query | `string` | no | ID or email of a known viewer. |
| `onlyWatched` | query | `boolean` | no | Return only views with percentWatched greater than 1. |
| `allViews` | query | `boolean` | no | Disable data pagination. |
