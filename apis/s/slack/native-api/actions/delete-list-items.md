# Delete List Items with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `slackLists.items.deleteMultiple`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Delete List Items](https://docs.slack.dev/reference/methods/slackLists.items.deleteMultiple/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `list_id` | body | `string` | yes |
| `ids[]` | body | `array<string>` | yes |
