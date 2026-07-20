# Lock Post with Discourse

Locks a Discourse post from being edited.

## Endpoint

- **Method:** `PUT`
- **Path:** `/posts/:id/locked.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Lock Post](https://docs.discourse.org/#tag/Posts/operation/lockPost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Post id. |
| `locked` | body | `boolean` | yes | Whether to lock the post. |
