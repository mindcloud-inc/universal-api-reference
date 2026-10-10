# Get List Item with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `slackLists.items.info`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Get List Item](https://docs.slack.dev/reference/methods/slackLists.items.info/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `list_id` | body | `string` | yes |
| `id` | body | `string` | yes |
| `include_is_subscribed` | body | `boolean` | no |
