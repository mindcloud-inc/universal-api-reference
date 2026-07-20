# Analyze keyword overlap and gaps with SE Ranking Data

Analyzes keyword overlap and gaps in SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/keywords/comparison`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Analyze keyword overlap and gaps](https://seranking.com/api/data/domain-analysis/#domain-comparison)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `compare` | query | `string` | yes | Competitor domain or URL for comparison (for example: example.com). |
| `domain` | query | `string` | yes | Primary domain for comparison (for example: seranking.com). |
| `source` | query | `string` | yes | Regional database code (for example: us). |
