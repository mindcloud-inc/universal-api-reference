# Intradesk: Copy Task

Copies an existing task in Intradesk.

```
POST https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/copy-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/copy-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/copy-task', {
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
| `body` | object | yes | TaskFormCopyModel JSON object request body documented by Intradesk Changes API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": 1,
      "correlationId": "string",
      "data": {},
      "errorMessage": "string",
      "errorType": 1,
      "id": 1,
      "isSuccess": true,
      "message": "string",
      "messages": {},
      "number": 1,
      "taskProcessType": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | number |  |
| `correlationId` | string |  |
| `data` | object |  |
| `errorMessage` | string |  |
| `errorType` | number |  |
| `id` | number |  |
| `isSuccess` | boolean |  |
| `message` | string |  |
| `messages` | object |  |
| `number` | number |  |
| `taskProcessType` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Intradesk API, this operation is `POST /changes/v1/Tasks/Copy` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-task.md) for the provider-specific parameters and requirements.

