# Get question keywords with SE Ranking Data

Retrieves question keywords from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/keywords/questions`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get question keywords](https://seranking.com/api/data/keyword-research/#questions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | yes | Keyword phrase (for example: seo tools). |
| `source` | query | `string` | yes | Regional database code (for example: us). |
