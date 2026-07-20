# Create Tagging with Feedbin

Creates a new tagging in Feedbin.

## Endpoint

- **Method:** `POST`
- **Path:** `taggings.json`
- **Base URL:** `https://api.feedbin.com/v2`
- **Official documentation:** [Create Tagging](https://github.com/feedbin/feedbin-api/blob/master/content/taggings.md#create-tagging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feed_id` | body | `number` | yes | Feedbin feed ID to tag. |
| `name` | body | `string` | yes | Tag name to apply to the feed. |
