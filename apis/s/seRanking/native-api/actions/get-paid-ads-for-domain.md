# Get paid ads for domain with SE Ranking Data

Retrieves paid ads for a domain from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/ads`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get paid ads for domain](https://seranking.com/api/data/domain-analysis/#paid-ads-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain to analyze (for example: seranking.com). |
| `source` | query | `string` | yes | Regional database code (for example: us). |
