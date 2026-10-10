# Update List Item Cells with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `slackLists.items.update`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Update List Item Cells](https://docs.slack.dev/reference/methods/slackLists.items.update/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | — |
| `cells[]` | body | `array<object>` | yes | — |
| `cells[].column_id` | body | `string` | yes | — |
| `cells[].row_id` | body | `string` | no | The item to update. Required unless Row ID to Create is enabled. |
| `cells[].row_id_to_create` | body | `boolean` | no | Create a new row for this cell instead of updating an existing item. |
| `cells[].rich_text[]` | body | `array<object>` | no | — |
| `cells[].rich_text[].type` | body | `list<string>` | no | Accepted values: `rich_text`. |
| `cells[].rich_text[].block_id` | body | `string` | no | Maximum length: 255. |
| `cells[].rich_text[].elements[]` | body | `array<object>` | no | — |
| `cells[].rich_text[].elements[].type` | body | `list<string>` | no | Accepted values: `rich_text_list`, `rich_text_preformatted`, `rich_text_quote`, `rich_text_section`. |
| `cells[].rich_text[].elements[].elements[]` | body | `array<object>` | no | — |
| `cells[].rich_text[].elements[].elements[].type` | body | `string` | no | — |
| `cells[].rich_text[].elements[].elements[].text` | body | `string` | no | — |
| `cells[].rich_text[].elements[].elements[].url` | body | `string` | no | — |
| `cells[].rich_text[].elements[].elements[].user_id` | body | `string` | no | — |
| `cells[].rich_text[].elements[].elements[].style` | body | `object` | no | — |
| `cells[].rich_text[].elements[].elements[].style.bold` | body | `boolean` | no | — |
| `cells[].rich_text[].elements[].elements[].style.italic` | body | `boolean` | no | — |
| `cells[].rich_text[].elements[].elements[].style.strike` | body | `boolean` | no | — |
| `cells[].rich_text[].elements[].elements[].style.code` | body | `boolean` | no | — |
| `cells[].user[]` | body | `array<string>` | no | — |
| `cells[].date[]` | body | `array<date>` | no | — |
| `cells[].select[]` | body | `array<string>` | no | — |
| `cells[].checkbox` | body | `boolean` | no | — |
| `cells[].number[]` | body | `array<number>` | no | — |
| `cells[].email[]` | body | `array<string>` | no | — |
| `cells[].phone[]` | body | `array<string>` | no | — |
| `cells[].attachment[]` | body | `array<string>` | no | — |
| `cells[].message[]` | body | `array<string>` | no | — |
| `cells[].rating[]` | body | `array<number>` | no | — |
| `cells[].timestamp[]` | body | `array<date>` | no | — |
| `cells[].channel[]` | body | `array<string>` | no | — |
| `cells[].link[]` | body | `array<object>` | no | — |
| `cells[].link[].original_url` | body | `string` | no | — |
| `cells[].link[].display_as_url` | body | `boolean` | no | — |
| `cells[].link[].display_name` | body | `string` | no | — |
| `cells[].reference[]` | body | `array<object>` | no | — |
| `cells[].reference[].file` | body | `object` | no | — |
| `cells[].reference[].file.file_id` | body | `string` | no | — |
