# Notion: Retrieve Block

Retrieves details for a block from Notion.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-block?connectionId=$CONNECTION_ID&blockId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blockId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-block?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blockId` | string | yes | ID of the block to retrieve. |

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

Through the native Notion API, this operation is `GET /blocks/:block_id` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-block.md) for the provider-specific parameters and requirements.

