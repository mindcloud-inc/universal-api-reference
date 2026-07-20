# Like Post with Discourse

Adds a like to a Discourse post.

## Endpoint

- **Method:** `POST`
- **Path:** `/post_actions.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Like Post](https://docs.discourse.org/#tag/Posts/operation/performPostAction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Post id to like. |
