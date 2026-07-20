# Get paid ads by keyword with SE Ranking Data

Retrieves paid ads by keyword from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/ads`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get paid ads by keyword](https://seranking.com/api/data/domain-analysis/#paid-ads-keyword)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | yes | Keyword to analyze paid ads for (for example: seo tools). |
| `source` | query | `string` | yes | Regional database code (for example: us). |
