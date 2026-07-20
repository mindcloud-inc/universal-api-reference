# Notion: Update Block

Updates an existing block in Notion.

```
PUT https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-block" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blockId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-block', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blockId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blockId` | string | yes | ID of the block to update. |
| `archived` | boolean | no | Set true to archive this block. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inTrash` | boolean | no | Set true to move this block to trash. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdBy": {},
      "createdTime": "2026-05-07T12:00:00.000Z",
      "hasChildren": true,
      "id": "string",
      "inTrash": true,
      "lastEditedBy": {},
      "lastEditedTime": "2026-05-07T12:00:00.000Z",
      "object": "string",
      "parent": {},
      "requestId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdBy` | object |  |
| `createdTime` | date |  |
| `hasChildren` | boolean |  |
| `id` | string |  |
| `inTrash` | boolean |  |
| `lastEditedBy` | object |  |
| `lastEditedTime` | date |  |
| `object` | string |  |
| `parent` | object |  |
| `requestId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Notion API, this operation is `PATCH /blocks/:block_id` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-block.md) for the provider-specific parameters and requirements.

