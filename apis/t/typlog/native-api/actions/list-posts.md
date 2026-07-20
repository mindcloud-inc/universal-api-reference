# List Posts with Typlog

Retrieves posts from Typlog.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [List Posts](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
| `cursor` | query | `number` | no | Pagination cursor. |
| `search` | query | `string` | no | Search term. |
