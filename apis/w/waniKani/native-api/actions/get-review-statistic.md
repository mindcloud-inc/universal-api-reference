# Get Review Statistic with WaniKani

Retrieves a review statistic from WaniKani.

## Endpoint

- **Method:** `GET`
- **Path:** `/review_statistics/[:id]`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [Get Review Statistic](https://docs.api.wanikani.com/20170710/#get-a-specific-review-statistic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique identifier of the review statistic. |
