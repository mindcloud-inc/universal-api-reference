# Create List Item with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `slackLists.items.create`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Create List Item](https://docs.slack.dev/reference/methods/slackLists.items.create/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | — |
| `duplicated_item_id` | body | `string` | no | Copy this existing item when creating the new item. |
| `parent_item_id` | body | `string` | no | Set to create a subtask under this item. |
| `initial_fields[]` | body | `array<object>` | no | — |
| `initial_fields[].column_id` | body | `string` | yes | — |
| `initial_fields[].rich_text[]` | body | `array<object>` | no | — |
| `initial_fields[].rich_text[].type` | body | `list<string>` | no | Accepted values: `rich_text`. |
| `initial_fields[].rich_text[].block_id` | body | `string` | no | Maximum length: 255. |
| `initial_fields[].rich_text[].elements[]` | body | `array<object>` | no | — |
| `initial_fields[].rich_text[].elements[].type` | body | `list<string>` | no | Accepted values: `rich_text_list`, `rich_text_preformatted`, `rich_text_quote`, `rich_text_section`. |
| `initial_fields[].rich_text[].elements[].elements[]` | body | `array<object>` | no | — |
| `initial_fields[].rich_text[].elements[].elements[].type` | body | `string` | no | — |
| `initial_fields[].rich_text[].elements[].elements[].text` | body | `string` | no | — |
| `initial_fields[].rich_text[].elements[].elements[].url` | body | `string` | no | — |
| `initial_fields[].rich_text[].elements[].elements[].user_id` | body | `string` | no | — |
| `initial_fields[].rich_text[].elements[].elements[].style` | body | `object` | no | — |
| `initial_fields[].rich_text[].elements[].elements[].style.bold` | body | `boolean` | no | — |
| `initial_fields[].rich_text[].elements[].elements[].style.italic` | body | `boolean` | no | — |
| `initial_fields[].rich_text[].elements[].elements[].style.strike` | body | `boolean` | no | — |
| `initial_fields[].rich_text[].elements[].elements[].style.code` | body | `boolean` | no | — |
| `initial_fields[].user[]` | body | `array<string>` | no | — |
| `initial_fields[].date[]` | body | `array<date>` | no | — |
| `initial_fields[].select[]` | body | `array<string>` | no | — |
| `initial_fields[].checkbox` | body | `boolean` | no | — |
| `initial_fields[].number[]` | body | `array<number>` | no | — |
| `initial_fields[].email[]` | body | `array<string>` | no | — |
| `initial_fields[].phone[]` | body | `array<string>` | no | — |
| `initial_fields[].attachment[]` | body | `array<string>` | no | — |
| `initial_fields[].message[]` | body | `array<string>` | no | — |
| `initial_fields[].rating[]` | body | `array<number>` | no | — |
| `initial_fields[].timestamp[]` | body | `array<date>` | no | — |
| `initial_fields[].channel[]` | body | `array<string>` | no | — |
| `initial_fields[].link[]` | body | `array<object>` | no | — |
| `initial_fields[].link[].original_url` | body | `string` | no | — |
| `initial_fields[].link[].display_as_url` | body | `boolean` | no | — |
| `initial_fields[].link[].display_name` | body | `string` | no | — |
| `initial_fields[].reference[]` | body | `array<object>` | no | — |
| `initial_fields[].reference[].file` | body | `object` | no | — |
| `initial_fields[].reference[].file.file_id` | body | `string` | no | — |
