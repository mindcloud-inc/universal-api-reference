# List Posts by Author with SCOTUSblog

## Endpoint

- **Method:** `GET`
- **Path:** `/author/:authorSlug/feed/`
- **Base URL:** `https://www.scotusblog.com`
- **Official documentation:** [List Posts by Author](https://www.scotusblog.com/2010/11/scotusblog-4-0-and-the-rss-feeds-feature/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorSlug` | path | `string` | yes | Author archive slug from the SCOTUSblog URL, for example adam-feldman. |
