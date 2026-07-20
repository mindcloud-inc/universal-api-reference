# Get Crawl Pages with Kadoa

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/crawl/:sessionId/pages`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Get Crawl Pages](https://docs.kadoa.com/api-reference/crawling/get-crawled-pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Crawl session ID |
| `currentPage` | query | `number` | no | Page number |
| `pageSize` | query | `number` | no | Results per page |
