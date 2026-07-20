# List Users with Slack

Retrieves users from a Slack workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `users.list`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [List Users](https://docs.slack.dev/reference/methods/users.list/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_locale` | query | `boolean` | no | Set this to true to receive the locale for users. Format: `toggle`. |
