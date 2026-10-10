# Slack: Create List Item



```
POST https://connect.mindcloud.co/v1/universal/slack/latest/actions/create-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slack/latest/actions/create-list-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "F12345678",
  "initialFields[].columnId": "Col12345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/create-list-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "F12345678",
    "initialFields[].columnId": "Col12345678"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Example: `F12345678`. |
| `initialFields[].columnId` | string | yes | Example: `Col12345678`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `duplicatedItemId` | string | no | Copy this existing item when creating the new item. |
| `parentItemId` | string | no | Set to create a subtask under this item. |
| `initialFields[]` | array<object> | no |  |
| `initialFields[].richText[]` | array<object> | no |  |
| `initialFields[].richText[].type` | list<string> | no | One of: `rich_text`. |
| `initialFields[].richText[].blockId` | string | no |  |
| `initialFields[].richText[].elements[]` | array<object> | no |  |
| `initialFields[].richText[].elements[].type` | list<string> | no | One of: `rich_text_list`, `rich_text_preformatted`, `rich_text_quote`, `rich_text_section`. |
| `initialFields[].richText[].elements[].elements[]` | array<object> | no |  |
| `initialFields[].richText[].elements[].elements[].type` | string | no |  |
| `initialFields[].richText[].elements[].elements[].text` | string | no |  |
| `initialFields[].richText[].elements[].elements[].url` | string | no |  |
| `initialFields[].richText[].elements[].elements[].userId` | string | no |  |
| `initialFields[].richText[].elements[].elements[].style` | object | no |  |
| `initialFields[].richText[].elements[].elements[].style.bold` | boolean | no |  |
| `initialFields[].richText[].elements[].elements[].style.italic` | boolean | no |  |
| `initialFields[].richText[].elements[].elements[].style.strike` | boolean | no |  |
| `initialFields[].richText[].elements[].elements[].style.code` | boolean | no |  |
| `initialFields[].user[]` | array<string> | no |  |
| `initialFields[].date[]` | array<date> | no | Example: `2026-10-15`. |
| `initialFields[].select[]` | array<string> | no |  |
| `initialFields[].checkbox` | boolean | no |  |
| `initialFields[].number[]` | array<number> | no |  |
| `initialFields[].email[]` | array<string> | no |  |
| `initialFields[].phone[]` | array<string> | no |  |
| `initialFields[].attachment[]` | array<string> | no |  |
| `initialFields[].message[]` | array<string> | no |  |
| `initialFields[].rating[]` | array<number> | no |  |
| `initialFields[].timestamp[]` | array<date> | no |  |
| `initialFields[].channel[]` | array<string> | no |  |
| `initialFields[].link[]` | array<object> | no |  |
| `initialFields[].link[].originalUrl` | string | no |  |
| `initialFields[].link[].displayAsUrl` | boolean | no |  |
| `initialFields[].link[].displayName` | string | no |  |
| `initialFields[].reference[]` | array<object> | no |  |
| `initialFields[].reference[].file` | object | no |  |
| `initialFields[].reference[].file.fileId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Slack API returns.

## Native endpoint

Through the native Slack API, this operation is `POST slackLists.items.create` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list-item.md) for the provider-specific parameters and requirements.

