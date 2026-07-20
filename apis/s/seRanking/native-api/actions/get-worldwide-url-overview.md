# Get worldwide URL overview with SE Ranking Data

Retrieves a worldwide URL overview from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/overview/worldwide/url`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get worldwide URL overview](https://seranking.com/api/data/domain-analysis/#worldwide-aggregate-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | query | `string` | yes | Regional database code (for example: us). |
| `url` | query | `string` | yes | URL to analyze (for example: https://seranking.com). |
