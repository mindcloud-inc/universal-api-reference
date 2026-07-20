# Add Bookmark with Instapaper

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1/bookmarks/add`
- **Base URL:** `https://www.instapaper.com`
- **Official documentation:** [Add Bookmark](https://www.instapaper.com/developers/v1/full-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | body | `string` | no | Optional 1 or 0 value that archives the bookmark while adding it. |
| `content` | body | `string` | no | Optional full HTML content used when Instapaper cannot crawl the page itself. |
| `description` | body | `string` | no | Optional plaintext description or summary of the article. |
| `folder_id` | body | `string` | no | Optional destination folder ID from List Folders. |
| `is_private_from_source` | body | `string` | no | Optional short label that makes the bookmark private and requires content. |
| `resolve_final_url` | body | `string` | no | Optional 1 or 0 value that tells Instapaper whether to resolve redirects before saving. |
| `tags` | body | `string` | no | Optional JSON array of tag objects, for example [{"name":"Tag Name"}]. |
| `title` | body | `string` | no | Optional title. If omitted, Instapaper tries to detect it. |
| `url` | body | `string` | no | The URL to save, unless you are creating a private bookmark. |
