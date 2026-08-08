# Monday: Update Payment Status Sub-Item



```
PUT https://connect.mindcloud.co/v1/universal/monday/latest/actions/update-payment-status-sub-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/monday/latest/actions/update-payment-status-sub-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": 1,
  "boardId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monday/latest/actions/update-payment-status-sub-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": 1,
    "boardId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | number | yes |  |
| `boardId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creator": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "title": "string"
      },
      "email": "ava@example.com",
      "group": {
        "archived": true,
        "color": "string",
        "deleted": true,
        "id": "string",
        "title": "string"
      },
      "id": "string",
      "name": "Ava Chen",
      "state": "string",
      "updates": [
        {
          "body": "string",
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator.email` | string |  |
| `creator.id` | string |  |
| `creator.name` | string |  |
| `creator.title` | string |  |
| `email` | string |  |
| `group.archived` | boolean |  |
| `group.color` | string |  |
| `group.deleted` | boolean |  |
| `group.id` | string |  |
| `group.title` | string |  |
| `id` | string |  |
| `name` | string |  |
| `state` | string |  |
| `updates[].body` | string |  |
| `updates[].id` | string |  |

## Native endpoint

Through the native Monday API, this operation is `POST` (base URL `https://api.monday.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payment-status-sub-item.md) for the provider-specific parameters and requirements.

