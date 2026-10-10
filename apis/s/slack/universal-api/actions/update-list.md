# Slack: Update List



```
PUT https://connect.mindcloud.co/v1/universal/slack/latest/actions/update-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/slack/latest/actions/update-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "F12345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/update-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "F12345678"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Example: `F12345678`. |
| `name` | string | no |  |
| `todoMode` | boolean | no | Show or hide completion, assignee, and due-date columns. |

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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Slack API returns.

## Native endpoint

Through the native Slack API, this operation is `POST slackLists.update` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list.md) for the provider-specific parameters and requirements.

