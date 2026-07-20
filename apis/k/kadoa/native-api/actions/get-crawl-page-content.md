# Get Crawl Page Content with Kadoa

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/crawl/:sessionId/pages/:pageId`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Get Crawl Page Content](https://docs.kadoa.com/api-reference/crawling/get-crawled-page-meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Crawl session ID |
| `pageId` | path | `string` | yes | Page ID |
| `format` | query | `string` | no | Content format (HTML or Markdown) |
