# Teamhood: Update Item

Updates an existing item in Teamhood.

```
PUT https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamhood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | string | no | The Teamhood item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boardId": "string",
      "completed": true,
      "displayId": "string",
      "id": "string",
      "parentId": "string",
      "rowId": "string",
      "statusId": "string",
      "title": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boardId` | string | The board that owns the item. |
| `completed` | boolean | Whether the item is completed. |
| `displayId` | string | The Teamhood item display ID. |
| `id` | string | The Teamhood item ID. |
| `parentId` | string | The parent item ID when present. |
| `rowId` | string | The row that contains the item. |
| `statusId` | string | The current item status ID. |
| `title` | string | The updated item title. |
| `workspaceId` | string | The workspace that owns the item. |

## Native endpoint

Through the native Teamhood API, this operation is `PUT /items/:itemId` (base URL `https://api-mindcloud1.teamhood.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item.md) for the provider-specific parameters and requirements.

