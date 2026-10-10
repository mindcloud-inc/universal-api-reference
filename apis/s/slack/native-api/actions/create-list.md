# Create List with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `slackLists.create`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Create List](https://docs.slack.dev/reference/methods/slackLists.create/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
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
| `schema[]` | body | `array<object>` | no | — |
| `schema[].key` | body | `string` | yes | — |
| `schema[].name` | body | `string` | yes | — |
| `schema[].type` | body | `list<string>` | yes | Accepted values: `attachment`, `canvas`, `channel`, `checkbox`, `created_by`, `created_time`, `date`, `email`, `last_edited_by`, `last_edited_time`, `link`, `message`, `number`, `phone`, `rating`, `reference`, `select`, `text`, `user`, `vote`. |
| `schema[].is_primary_column` | body | `boolean` | no | Only one column may be primary, and it must be a text column. |
| `schema[].options` | body | `object` | no | — |
| `schema[].options.choices[]` | body | `array<object>` | no | — |
| `schema[].options.choices[].value` | body | `string` | no | — |
| `schema[].options.choices[].label` | body | `string` | no | — |
| `schema[].options.choices[].color` | body | `list<string>` | no | Accepted values: `blue`, `brown`, `cyan`, `gray`, `green`, `indigo`, `orange`, `pink`, `purple`, `red`, `yellow`. |
| `schema[].options.format` | body | `list<string>` | no | Accepted values: `multi_entity`, `multi_select`, `single_entity`, `single_select`. |
| `schema[].options.precision` | body | `number` | no | — |
| `schema[].options.date_format` | body | `list<string>` | no | Accepted values: `DD MMMM YYYY`, `DD/MM/YYYY`, `MM/DD/YYYY`, `MMMM DD, YYYY`, `YYYY/MM/DD`, `default`. |
| `schema[].options.emoji` | body | `string` | no | — |
| `schema[].options.emoji_team_id` | body | `string` | no | — |
| `schema[].options.max` | body | `number` | no | — |
| `schema[].options.default_value_typed` | body | `object` | no | — |
| `schema[].options.default_value_typed.user[]` | body | `array<string>` | no | — |
| `schema[].options.default_value_typed.channel[]` | body | `array<string>` | no | — |
| `schema[].options.default_value_typed.select[]` | body | `array<string>` | no | — |
| `schema[].options.show_member_name` | body | `boolean` | no | — |
| `schema[].options.notify_users` | body | `boolean` | no | — |
| `copy_from_list_id` | body | `string` | no | — |
| `include_copied_list_records` | body | `boolean` | no | — |
| `todo_mode` | body | `boolean` | no | Adds completion, assignee, and due-date columns for task tracking. |
