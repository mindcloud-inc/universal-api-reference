# Reorder Notes with Collected Notes

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:siteId/notes/reorder`
- **Base URL:** `https://collectednotes.com`
- **Official documentation:** [Reorder Notes](https://collectednotes.com/blog/api#reorder-notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `number` | yes | The Collected Notes site ID. |
| `ids` | query | `string` | yes | Send the sorted note IDs as a JSON-like array string, for example [1,2,3]. |
