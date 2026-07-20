# Search Channels and Users with Slack

Finds Slack channels and users by search query.

## Endpoint

- **Method:** `POST`
- **Path:** `assistant.search.context`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Search Channels and Users](https://docs.slack.dev/reference/methods/assistant.search.context/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | User prompt or search query |
