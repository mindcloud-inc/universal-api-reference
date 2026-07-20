# Get Storage Item with Crawlbase

Retrieves a stored page from Crawlbase.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage`
- **Base URL:** `https://api.crawlbase.com`
- **Official documentation:** [Get Storage Item](https://crawlbase.com/docs/cloud-storage/parameters/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rid` | query | `string` | no | Request identifier for the stored item. Provide either RID or URL. |
| `url` | query | `string` | no | Crawled URL for the stored item. Provide either URL or RID. |
