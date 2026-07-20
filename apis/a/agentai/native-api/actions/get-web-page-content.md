# Get Web Page Content with Agent.ai

Retrieves web page text from Agent.ai by URL or domain.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/grab_web_text`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Get Web Page Content](https://docs.agent.ai/api-reference/get-data/web-page-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the web page to extract text from. |
| `mode` | body | `string` | no | Crawler mode: scrape for one page, crawl for up to 100 pages. |
