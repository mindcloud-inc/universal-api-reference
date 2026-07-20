# Rename Tag with Feedbin

Renames an existing tag in Feedbin.

## Endpoint

- **Method:** `POST`
- **Path:** `tags.json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Rename Tag](https://github.com/feedbin/feedbin-api/blob/master/content/tags.md#post-v2tagsjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `old_name` | body | `string` | yes | Existing tag name to rename. |
| `new_name` | body | `string` | yes | New tag name. |
