# Intradesk: Log Task Inventory

Logs task inventory usage in Intradesk.

```
POST https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/log-task-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/log-task-inventory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/log-task-inventory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | TaskInventoryRequestModel JSON object request body documented by Intradesk Changes API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorMessage": "string",
      "id": 1,
      "inventories": [
        {}
      ],
      "isSuccess": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorMessage` | string |  |
| `id` | number |  |
| `inventories` | array<object> |  |
| `isSuccess` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Intradesk API, this operation is `PUT /changes/v1/TaskInventory` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/log-task-inventory.md) for the provider-specific parameters and requirements.

