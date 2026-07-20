# Search Notes with Collected Notes

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:siteId/notes/search`
- **Base URL:** `https://collectednotes.com`
- **Official documentation:** [Search Notes](https://collectednotes.com/blog/api#search-notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `number` | yes | The Collected Notes site ID. |
| `term` | query | `string` | yes | The term to search for in the site's notes. |
