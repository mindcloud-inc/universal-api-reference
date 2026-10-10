# Delete List Item with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `slackLists.items.delete`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Delete List Item](https://docs.slack.dev/reference/methods/slackLists.items.delete/)

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
