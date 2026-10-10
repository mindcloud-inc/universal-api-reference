# List Items with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `slackLists.items.list`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [List Items](https://docs.slack.dev/reference/methods/slackLists.items.list/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | — |
| `archived` | body | `boolean` | no | — |
| `include_list` | body | `boolean` | no | Return the list title, column definitions, and row count alongside its items. |
