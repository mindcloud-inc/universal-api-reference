# Get domain competitors with SE Ranking Data

Retrieves domain competitors from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/competitors`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get domain competitors](https://seranking.com/api/data/domain-analysis/#competitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain to analyze (for example: seranking.com). |
| `source` | query | `string` | yes | Regional database code (for example: us). |
