# List Latest Topics with Discourse

Retrieves the latest topics from Discourse.

## Endpoint

- **Method:** `GET`
- **Path:** `/latest.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [List Latest Topics](https://docs.discourse.org/#tag/Topics/operation/listLatestTopics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ascending` | query | `string` | no | Set to true to sort ascending. |
| `order` | query | `string` | no | Sort order for latest topics, such as default, created, or activity. |
