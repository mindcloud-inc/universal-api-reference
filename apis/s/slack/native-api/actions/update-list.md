# Update List with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `slackLists.update`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Update List](https://docs.slack.dev/reference/methods/slackLists.update/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | — |
| `name` | body | `string` | no | — |
| `description_blocks[]` | body | `array<object>` | no | — |
| `description_blocks[].type` | body | `list<string>` | no | Accepted values: `rich_text`. |
| `description_blocks[].block_id` | body | `string` | no | Maximum length: 255. |
| `description_blocks[].elements[]` | body | `array<object>` | no | — |
| `description_blocks[].elements[].type` | body | `list<string>` | no | Accepted values: `rich_text_list`, `rich_text_preformatted`, `rich_text_quote`, `rich_text_section`. |
| `description_blocks[].elements[].elements[]` | body | `array<object>` | no | — |
| `description_blocks[].elements[].elements[].type` | body | `string` | no | — |
| `description_blocks[].elements[].elements[].text` | body | `string` | no | — |
| `description_blocks[].elements[].elements[].url` | body | `string` | no | — |
| `description_blocks[].elements[].elements[].user_id` | body | `string` | no | — |
| `description_blocks[].elements[].elements[].style` | body | `object` | no | — |
| `description_blocks[].elements[].elements[].style.bold` | body | `boolean` | no | — |
| `description_blocks[].elements[].elements[].style.italic` | body | `boolean` | no | — |
| `description_blocks[].elements[].elements[].style.strike` | body | `boolean` | no | — |
| `description_blocks[].elements[].elements[].style.code` | body | `boolean` | no | — |
| `todo_mode` | body | `boolean` | no | Show or hide completion, assignee, and due-date columns. |
