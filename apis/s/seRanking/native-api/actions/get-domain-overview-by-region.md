# Get Domain Overview by Region with SE Ranking Data

Retrieves a regional domain overview from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/overview/db`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get Domain Overview by Region](https://seranking.com/api/data/domain-analysis/#regional-database)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | query | `string` | yes | Database region code (for example: us, gb). |
| `domain` | query | `string` | yes | Domain to analyze (for example: seranking.com). |
| `with_subdomains` | query | `list<string>` | no | Include subdomain data (1/0). Accepted values: `0`, `1`. |
