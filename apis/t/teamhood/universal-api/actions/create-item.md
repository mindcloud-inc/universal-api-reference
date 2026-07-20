# Teamhood: Create Item

Creates a new item in Teamhood.

```
POST https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamhood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/create-item', {
  method: 'POST',
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
| `boardId` | string | no | The board that will own the item. |
| `rowId` | string | no | The row that will contain the item. |
| `statusId` | string | no | The initial status for the item. |
| `title` | string | no | The item title. |
| `workspaceId` | string | no | The workspace that will own the item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boardId": "string",
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
| `displayId` | string | The Teamhood item display ID. |
| `id` | string | The Teamhood item ID. |
| `parentId` | string | The parent item ID when the item is created as a child. |
| `rowId` | string | The row that contains the item. |
| `statusId` | string | The current item status ID. |
| `title` | string | The item title. |
| `workspaceId` | string | The workspace that owns the item. |

## Native endpoint

Through the native Teamhood API, this operation is `POST /items` (base URL `https://api-mindcloud1.teamhood.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.

