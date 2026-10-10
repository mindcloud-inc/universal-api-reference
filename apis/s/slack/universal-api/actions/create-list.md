# Slack: Create List



```
POST https://connect.mindcloud.co/v1/universal/slack/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slack/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "schema[].key": "string",
  "schema[].name": "Ava Chen",
  "schema[].type": "attachment"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "schema[].key": "string",
    "schema[].name": "Ava Chen",
    "schema[].type": "attachment"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `todoMode` | boolean | no | Adds completion, assignee, and due-date columns for task tracking. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `descriptionBlocks[]` | array<object> | no |  |
| `descriptionBlocks[].type` | list<string> | no | One of: `rich_text`. |
| `descriptionBlocks[].blockId` | string | no |  |
| `descriptionBlocks[].elements[]` | array<object> | no |  |
| `descriptionBlocks[].elements[].type` | list<string> | no | One of: `rich_text_list`, `rich_text_preformatted`, `rich_text_quote`, `rich_text_section`. |
| `descriptionBlocks[].elements[].elements[]` | array<object> | no |  |
| `descriptionBlocks[].elements[].elements[].type` | string | no |  |
| `descriptionBlocks[].elements[].elements[].text` | string | no |  |
| `descriptionBlocks[].elements[].elements[].url` | string | no |  |
| `descriptionBlocks[].elements[].elements[].userId` | string | no |  |
| `descriptionBlocks[].elements[].elements[].style` | object | no |  |
| `descriptionBlocks[].elements[].elements[].style.bold` | boolean | no |  |
| `descriptionBlocks[].elements[].elements[].style.italic` | boolean | no |  |
| `descriptionBlocks[].elements[].elements[].style.strike` | boolean | no |  |
| `descriptionBlocks[].elements[].elements[].style.code` | boolean | no |  |
| `schema[]` | array<object> | no |  |
| `schema[].key` | string | yes |  |
| `schema[].name` | string | yes |  |
| `schema[].type` | list<string> | yes | One of: `attachment`, `canvas`, `channel`, `checkbox`, `created_by`, `created_time`, `date`, `email`, `last_edited_by`, `last_edited_time`, `link`, `message`, `number`, `phone`, `rating`, `reference`, `select`, `text`, `user`, `vote`. |
| `schema[].isPrimaryColumn` | boolean | no | Only one column may be primary, and it must be a text column. |
| `schema[].options` | object | no |  |
| `schema[].options.choices[]` | array<object> | no |  |
| `schema[].options.choices[].value` | string | no |  |
| `schema[].options.choices[].label` | string | no |  |
| `schema[].options.choices[].color` | list<string> | no | One of: `blue`, `brown`, `cyan`, `gray`, `green`, `indigo`, `orange`, `pink`, `purple`, `red`, `yellow`. |
| `schema[].options.format` | list<string> | no | One of: `multi_entity`, `multi_select`, `single_entity`, `single_select`. |
| `schema[].options.precision` | number | no |  |
| `schema[].options.dateFormat` | list<string> | no | One of: `DD MMMM YYYY`, `DD/MM/YYYY`, `MM/DD/YYYY`, `MMMM DD, YYYY`, `YYYY/MM/DD`, `default`. |
| `schema[].options.emoji` | string | no | Example: `:star:`. |
| `schema[].options.emojiTeamId` | string | no |  |
| `schema[].options.max` | number | no |  |
| `schema[].options.defaultValueTyped` | object | no |  |
| `schema[].options.defaultValueTyped.user[]` | array<string> | no |  |
| `schema[].options.defaultValueTyped.channel[]` | array<string> | no |  |
| `schema[].options.defaultValueTyped.select[]` | array<string> | no |  |
| `schema[].options.showMemberName` | boolean | no |  |
| `schema[].options.notifyUsers` | boolean | no |  |
| `copyFromListId` | string | no | Example: `F12345678`. |
| `includeCopiedListRecords` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Slack API returns.

## Native endpoint

Through the native Slack API, this operation is `POST slackLists.create` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

