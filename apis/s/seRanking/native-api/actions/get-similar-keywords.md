# Get similar keywords with SE Ranking Data

Retrieves similar keywords from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/keywords/similar`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get similar keywords](https://seranking.com/api/data/keyword-research/#similar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | yes | Keyword phrase (for example: seo tools). |
| `source` | query | `string` | yes | Regional database code (for example: us). |
