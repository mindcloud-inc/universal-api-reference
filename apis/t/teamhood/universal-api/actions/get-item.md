# Teamhood: Get Item

Retrieves item details from Teamhood by ID.

```
GET https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamhood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/get-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/get-item?${params}`, {
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
| `itemId` | string | no | The Teamhood item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedUserId": "string",
      "boardId": "string",
      "completed": true,
      "displayId": "string",
      "id": "string",
      "ownerId": "string",
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
| `assignedUserId` | string | The assigned user ID when present. |
| `boardId` | string | The board that owns the item. |
| `completed` | boolean | Whether the item is completed. |
| `displayId` | string | The Teamhood item display ID. |
| `id` | string | The Teamhood item ID. |
| `ownerId` | string | The item owner user ID when present. |
| `rowId` | string | The row that contains the item. |
| `statusId` | string | The current item status ID. |
| `title` | string | The item title. |
| `workspaceId` | string | The workspace that owns the item. |

## Native endpoint

Through the native Teamhood API, this operation is `GET /items/:itemId` (base URL `https://api-mindcloud1.teamhood.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

