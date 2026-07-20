# List Scheduled Messages with Slack

Retrieves scheduled messages from a Slack workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `chat.scheduledMessages.list`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [List Scheduled Messages](https://docs.slack.dev/reference/methods/chat.scheduledMessages.list/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list` | no | Channel to send the message to. |
| `latest` | body | `date` | no | A Unix timestamp of the latest value in the time range |
| `oldest` | body | `date` | no | A Unix timestamp of the oldest value in the time range |
