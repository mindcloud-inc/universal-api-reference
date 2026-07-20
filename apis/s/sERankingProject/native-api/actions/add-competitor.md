# Add Competitor with SE Ranking Project

Creates a tracked competitor in SE Ranking.

## Endpoint

- **Method:** `POST`
- **Path:** `/competitors`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [Add Competitor](https://seranking.com/api/project/competitors/#add-competitor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | body | `list<number>` | yes | Project site ID. |
| `url` | body | `string` | yes | Competitor website URL. |
| `name` | body | `string` | no | Competitor website name. |
| `subdomain_match` | body | `number` | no | Include subdomains flag (1 or 0). |
