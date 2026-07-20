# List All Website Domain Research Reports with PagePixels

## Endpoint

- **Method:** `GET`
- **Path:** `/api/domain_research_requests`
- **Base URL:** `https://api.pagepixels.com`
- **Official documentation:** [List All Website Domain Research Reports](https://pagepixels.com/app/screenshots-api-documentation#list-all-domain-research-reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | The page to retrieve. |
| `limit` | query | `number` | no | The maximum number of reports to return. |
| `after` | query | `number` | no | Only return reports created after this unix timestamp. |
| `before` | query | `number` | no | Only return reports created before this unix timestamp. |
| `order` | query | `string` | no | Sort order: ASC or DESC. |
