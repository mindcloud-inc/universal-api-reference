# List Channel Messages with Slack

Retrieves channel messages and events from Slack.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations.history`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [List Channel Messages](https://docs.slack.dev/reference/methods/conversations.history/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list` | yes | Conversation ID to fetch history for. |
| `include_all_metadata` | body | `boolean` | no | Return all metadata associated with this message. Format: `toggle`. |
| `inclusive` | body | `boolean` | no | Include messages with oldest or latest timestamps in results. Ignored unless either timestamp is specified. Format: `toggle`. |
| `latest` | body | `date` | no | Only messages before this Unix timestamp will be included in results. |
| `oldest` | body | `date` | no | Only messages after this Unix timestamp will be included in results. |
