# Digiclose: Create Task



```
POST https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assigneeId": 1,
  "categoryId": 1,
  "contactId": 1,
  "creatorId": 1,
  "description": "string",
  "dueAt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assigneeId": 1,
    "categoryId": 1,
    "contactId": 1,
    "creatorId": 1,
    "description": "string",
    "dueAt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigneeId` | number | yes |  |
| `categoryId` | number | yes |  |
| `contactId` | number | yes |  |
| `creatorId` | number | yes |  |
| `description` | string | yes |  |
| `dueAt` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "taskId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `taskId` | number |  |

## Native endpoint

Through the native Digiclose API, this operation is `POST /tasks` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

