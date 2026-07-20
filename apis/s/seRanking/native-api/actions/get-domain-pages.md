# Get domain pages with SE Ranking Data

Retrieves domain pages from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/pages`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get domain pages](https://seranking.com/api/data/domain-analysis/#domain-pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scope` | query | `list<string>` | yes | Analysis scope (for example: domain). Accepted values: `base_domain`, `domain`, `exact_url`, `path`, `subdomain`. |
| `source` | query | `string` | yes | Regional database code (for example: us). |
| `target` | query | `string` | yes | Target domain or URL (for example: seranking.com). |
