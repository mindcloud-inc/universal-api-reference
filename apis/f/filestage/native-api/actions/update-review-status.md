# Update Review Status with Filestage

Updates a review status in Filestage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/reviews/{reviewId}/status`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Update Review Status](https://developers.filestage.io/docs/api/txazpofppz8rd-update-review-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewId` | path | `string` | yes | Review Id |
| `state` | body | `string` | yes | — |
