# Create Topic with Discourse

Creates a new topic in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create Topic](https://docs.discourse.org/#tag/Posts/operation/createTopicPostPM)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Topic title. Required when creating a new topic. |
| `raw` | body | `string` | yes | Topic body in raw Discourse markdown. |
| `category` | body | `number` | no | Optional category id for the new topic. |
| `external_id` | body | `string` | no | Optional external system id to associate with the new topic. |
| `auto_track` | body | `boolean` | no | Set false to avoid automatically tracking the new topic. |
