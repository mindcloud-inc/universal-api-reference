# Update Topic with Discourse

Updates an existing topic in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/t/-/:id.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update Topic](https://docs.discourse.org/#tag/Topics/operation/updateTopic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Topic id. |
| `topic.category_id` | body | `number` | no | Updated category id for the topic. |
| `topic.title` | body | `string` | no | Updated topic title. |
