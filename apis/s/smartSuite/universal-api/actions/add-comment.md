# SmartSuite: Add Comment

Creates a new comment in SmartSuite.

```
POST https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/add-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recordId": "69b45da87cb40fc74dbb4b8c",
  "tableId": "69b45da87cb40fc74dbb4b84",
  "messageHtml": "<p>MC Test Comment 2</p>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recordId": "69b45da87cb40fc74dbb4b8c",
    "tableId": "69b45da87cb40fc74dbb4b84",
    "messageHtml": "<p>MC Test Comment 2</p>"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string | yes | The SmartSuite record ID to add the comment to. Example: `69b45da87cb40fc74dbb4b8c`. |
| `tableId` | string | yes | The SmartSuite table ID that owns the record. Example: `69b45da87cb40fc74dbb4b84`. |
| `messageHtml` | string | yes | The comment body as HTML, for example `<p>Hello</p>`. Example: `<p>MC Test Comment 2</p>`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedTo` | string | no | Optional SmartSuite assignee member ID for the comment. |
| `parentComment` | string | no | Optional parent comment ID when replying to an existing comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application": "string",
      "assignedTo": {},
      "createdOn": "string",
      "deletedOn": {},
      "email": {},
      "fieldSlug": {},
      "followers": [
        "string"
      ],
      "id": "string",
      "key": 1,
      "member": "string",
      "message": {
        "data": {
          "content": [
            {
              "content": [
                {
                  "text": "string",
                  "type": "string"
                }
              ],
              "type": "string"
            }
          ],
          "type": "string"
        },
        "html": "string",
        "preview": "string"
      },
      "parentComment": {},
      "record": "string",
      "resolvedBy": {},
      "solution": "string",
      "type": "string",
      "updatedOn": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application` | string |  |
| `assignedTo` | object |  |
| `createdOn` | string |  |
| `deletedOn` | object |  |
| `email` | object |  |
| `fieldSlug` | object |  |
| `followers[]` | string |  |
| `id` | string |  |
| `key` | number |  |
| `member` | string |  |
| `message.data.content[].content[].text` | string |  |
| `message.data.content[].content[].type` | string |  |
| `message.data.content[].type` | string |  |
| `message.data.type` | string |  |
| `message.html` | string |  |
| `message.preview` | string |  |
| `parentComment` | object |  |
| `record` | string |  |
| `resolvedBy` | object |  |
| `solution` | string |  |
| `type` | string |  |
| `updatedOn` | object |  |

## Native endpoint

Through the native SmartSuite API, this operation is `POST /comments/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-comment.md) for the provider-specific parameters and requirements.

