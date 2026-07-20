# Bookmark Topic with Discourse

Adds a bookmark to a Discourse topic.

## Endpoint

- **Method:** `PUT`
- **Path:** `/t/:id/bookmark.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Bookmark Topic](https://docs.discourse.org/#tag/Topics/operation/bookmarkTopic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Topic id to bookmark. |
