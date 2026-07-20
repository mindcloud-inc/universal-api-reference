# Discover brand by URL with SE Ranking Data

Discovers a brand by URL in SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ai-search/discover-brand`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Discover brand by URL](https://seranking.com/api/data/ai-search/#discover-brand-by-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scope` | query | `list<string>` | yes | Analysis scope (for example: base_domain). Accepted values: `base_domain`, `domain`, `exact_url`, `path`, `subdomain`. |
| `source` | query | `string` | yes | Regional source code (for example: us). |
| `target` | query | `string` | yes | Target domain or URL (for example: seranking.com). |
