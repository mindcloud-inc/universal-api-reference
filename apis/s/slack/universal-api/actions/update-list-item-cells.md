# Slack: Update List Item Cells



```
PUT https://connect.mindcloud.co/v1/universal/slack/latest/actions/update-list-item-cells
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/slack/latest/actions/update-list-item-cells" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "F12345678",
  "cells[]": [
    {}
  ],
  "cells[].columnId": "Col12345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/update-list-item-cells', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "F12345678",
    "cells[]": [{}],
    "cells[].columnId": "Col12345678"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Example: `F12345678`. |
| `cells[]` | array<object> | yes |  |
| `cells[].columnId` | string | yes | Example: `Col12345678`. |
| `cells[].rowId` | string | no | The item to update. Required unless Row ID to Create is enabled. Example: `Rec12345678`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cells[].rowIdToCreate` | boolean | no | Create a new row for this cell instead of updating an existing item. |
| `cells[].richText[]` | array<object> | no |  |
| `cells[].richText[].type` | list<string> | no | One of: `rich_text`. |
| `cells[].richText[].blockId` | string | no |  |
| `cells[].richText[].elements[]` | array<object> | no |  |
| `cells[].richText[].elements[].type` | list<string> | no | One of: `rich_text_list`, `rich_text_preformatted`, `rich_text_quote`, `rich_text_section`. |
| `cells[].richText[].elements[].elements[]` | array<object> | no |  |
| `cells[].richText[].elements[].elements[].type` | string | no |  |
| `cells[].richText[].elements[].elements[].text` | string | no |  |
| `cells[].richText[].elements[].elements[].url` | string | no |  |
| `cells[].richText[].elements[].elements[].userId` | string | no |  |
| `cells[].richText[].elements[].elements[].style` | object | no |  |
| `cells[].richText[].elements[].elements[].style.bold` | boolean | no |  |
| `cells[].richText[].elements[].elements[].style.italic` | boolean | no |  |
| `cells[].richText[].elements[].elements[].style.strike` | boolean | no |  |
| `cells[].richText[].elements[].elements[].style.code` | boolean | no |  |
| `cells[].user[]` | array<string> | no |  |
| `cells[].date[]` | array<date> | no | Example: `2026-10-15`. |
| `cells[].select[]` | array<string> | no |  |
| `cells[].checkbox` | boolean | no |  |
| `cells[].number[]` | array<number> | no |  |
| `cells[].email[]` | array<string> | no |  |
| `cells[].phone[]` | array<string> | no |  |
| `cells[].attachment[]` | array<string> | no |  |
| `cells[].message[]` | array<string> | no |  |
| `cells[].rating[]` | array<number> | no |  |
| `cells[].timestamp[]` | array<date> | no |  |
| `cells[].channel[]` | array<string> | no |  |
| `cells[].link[]` | array<object> | no |  |
| `cells[].link[].originalUrl` | string | no |  |
| `cells[].link[].displayAsUrl` | boolean | no |  |
| `cells[].link[].displayName` | string | no |  |
| `cells[].reference[]` | array<object> | no |  |
| `cells[].reference[].file` | object | no |  |
| `cells[].reference[].file.fileId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Slack API returns.

## Native endpoint

Through the native Slack API, this operation is `POST slackLists.items.update` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list-item-cells.md) for the provider-specific parameters and requirements.

