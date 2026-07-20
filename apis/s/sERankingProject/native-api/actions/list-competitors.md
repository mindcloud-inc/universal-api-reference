# List Competitors with SE Ranking Project

Retrieves project competitors from SE Ranking.

## Endpoint

- **Method:** `GET`
- **Path:** `/competitors/site/:site_id`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [List Competitors](https://seranking.com/api/project/competitors/#list-competitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<number>` | yes | Project site identifier from SE Ranking. |
