# Intradesk: List Task Relations

Retrieves task relations from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-relations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-relations?connectionId=$CONNECTION_ID&taskNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-relations?${params}`, {
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
| `taskNumber` | string | yes | Task number from Intradesk TaskForm API path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "tree": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `tree` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /taskform/api/TaskRelations/{taskNumber}` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-relations.md) for the provider-specific parameters and requirements.

