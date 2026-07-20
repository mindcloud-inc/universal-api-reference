# Get domain subdomains with SE Ranking Data

Retrieves domain subdomains from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain/subdomains`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get domain subdomains](https://seranking.com/api/data/domain-analysis/#domain-subdomains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | query | `list<string>` | yes | Sort order: asc or desc. Accepted values: `asc`, `desc`. |
| `page` | query | `string` | no | Page number for pagination. |
| `scope` | query | `list<string>` | yes | Analysis scope (for example: domain). Accepted values: `base_domain`, `domain`, `exact_url`, `path`, `subdomain`. |
| `sort` | query | `list<string>` | yes | Sort field (for example: traffic, keywords_count, backlinks_count). Accepted values: `backlinks_count`, `keywords_count`, `traffic`. |
| `source` | query | `string` | yes | Regional database code (for example: us). |
| `target` | query | `string` | yes | Target domain or URL (for example: seranking.com). |
