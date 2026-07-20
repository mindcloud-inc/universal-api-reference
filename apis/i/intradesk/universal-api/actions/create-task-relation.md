# Intradesk: Create Task Relation

Creates a task relation in Intradesk.

```
POST https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/create-task-relation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/create-task-relation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/create-task-relation', {
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
| `body` | object | yes | TaskRelationsSimpleRequestModel JSON object request body documented by Intradesk Changes API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "correlationId": "string",
      "data": {},
      "errorType": 1,
      "id": 1,
      "isSuccess": true,
      "message": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `correlationId` | string |  |
| `data` | object |  |
| `errorType` | number |  |
| `id` | number |  |
| `isSuccess` | boolean |  |
| `message` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Intradesk API, this operation is `POST /changes/v1/TaskRelations` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-relation.md) for the provider-specific parameters and requirements.

