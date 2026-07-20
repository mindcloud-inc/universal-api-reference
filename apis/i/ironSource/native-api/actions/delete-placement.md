# Delete Placement with ironSource

Deletes an existing placement from ironSource by archiving it.

## Endpoint

- **Method:** `DELETE`
- **Path:** `partners/publisher/placements/v1`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Delete Placement](https://docs.unity.com/en-us/grow/levelplay/platform/api/placements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adUnit` | body | `string` | no | Ad unit name: rewardedVideo, interstitial, or banner. |
| `appKey` | body | `string` | no | Application key to archive the placement for. |
| `id` | body | `string` | no | Placement ID to archive. |
