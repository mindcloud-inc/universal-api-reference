# List Posts by Category with SCOTUSblog

## Endpoint

- **Method:** `GET`
- **Path:** `/category/:categorySlug/feed/`
- **Base URL:** `https://www.scotusblog.com`
- **Official documentation:** [List Posts by Category](https://www.scotusblog.com/2010/11/scotusblog-4-0-and-the-rss-feeds-feature/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categorySlug` | path | `string` | yes | Category archive slug from the SCOTUSblog URL, for example court-news. |
