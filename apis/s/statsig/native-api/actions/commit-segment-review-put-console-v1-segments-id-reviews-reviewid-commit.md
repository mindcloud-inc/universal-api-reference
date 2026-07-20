# Commit Segment Review with Statsig

Commits a segment review in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/segments/{id}/reviews/{reviewID}/commit`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Commit Segment Review](https://docs.statsig.com/api-reference/segments/commit-segment-review)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `reviewID` | path | `string` | yes |
