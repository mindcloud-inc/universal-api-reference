# Update Topic Timestamp with Discourse

Updates the timestamp of a Discourse topic.

## Endpoint

- **Method:** `PUT`
- **Path:** `/t/:id/change-timestamp.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update Topic Timestamp](https://docs.discourse.org/#tag/Topics/operation/updateTopicTimestamp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Topic id. |
| `timestamp` | body | `string` | yes | Unix timestamp string for the topic timestamp update. |
