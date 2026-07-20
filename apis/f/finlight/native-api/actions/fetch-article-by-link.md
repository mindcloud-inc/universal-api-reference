# Fetch Article By Link with finlight

Retrieves a single finlight article by URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/articles/by-link`
- **Base URL:** `https://api.finlight.me`
- **Official documentation:** [Fetch Article By Link](https://docs.finlight.me/v2/rest-endpoints/#fetch-article-by-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `link` | query | `string` | yes | Article URL to look up. |
| `includeContent` | query | `boolean` | no | Include the full article content in the response. |
| `includeEntities` | query | `boolean` | no | Include company entities when the subscription tier supports them. |
