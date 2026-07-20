# MoreApp: Revoke Task

Revokes a task in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/revoke-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/revoke-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "209321",
  "formId": "69bc27abd8b8b4ce5be6b2ba",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/revoke-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "209321",
    "formId": "69bc27abd8b8b4ce5be6b2ba",
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `formId` | string | yes | MoreApp form identifier. Default: `69bc27abd8b8b4ce5be6b2ba`. |
| `taskId` | string | yes | MoreApp task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "message": "string",
      "scope": "string",
      "status": 1,
      "traceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object | Additional provider error details when present. |
| `message` | string | Provider message describing the revoke task outcome. |
| `scope` | string | MoreApp error scope for the revoke task response. |
| `status` | number | HTTP-style provider status returned when the revoke request fails. |
| `traceId` | string | MoreApp trace identifier for support and debugging. |

## Native endpoint

Through the native MoreApp API, this operation is `POST /api/v1.0/customers/{{customerId}}/{{formId}}/tasks/{{taskId}}/revoke` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-task.md) for the provider-specific parameters and requirements.

