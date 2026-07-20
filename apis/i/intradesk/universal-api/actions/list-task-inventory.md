# Intradesk: List Task Inventory

Retrieves task inventory from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-inventory?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-inventory?${params}`, {
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
| `taskId` | string | yes | Task identifier from Intradesk TaskForm API path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "customerId": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isArchived": true,
      "measureUnit": "string",
      "taskId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "userId": 1,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `customerId` | number |  |
| `date` | date |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `measureUnit` | string |  |
| `taskId` | number |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `userId` | number |  |
| `userName` | string |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /taskform/api/TaskInventory/{taskId}` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-inventory.md) for the provider-specific parameters and requirements.

