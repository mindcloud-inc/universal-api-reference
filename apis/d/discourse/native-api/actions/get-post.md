# Get Post with Discourse

Retrieves a single post from Discourse.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/:id.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Get Post](https://docs.discourse.org/#tag/Posts/operation/getPost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Numeric Discourse post ID. |
