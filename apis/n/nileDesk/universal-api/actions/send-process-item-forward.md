# NileDesk: Send Process Item Forward

Sends a process item forward in NileDesk.

```
PUT https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/send-process-item-forward
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NileDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/send-process-item-forward" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "process_id": "string",
  "step_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/send-process-item-forward', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "process_id": "string",
    "step_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form_fields` | object | no | Optional process form field values keyed by NileDesk field identifier. |
| `form_tables` | object | no | Optional embedded table payload keyed by collection name. |
| `process_id` | string | yes | The NileDesk process item to move forward. |
| `remarks` | string | no | Optional remarks to store with the transition. |
| `step_id` | string | yes | The NileDesk step identifier the item should process from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message describing the result. |
| `success` | boolean | Whether NileDesk accepted the request. |

## Native endpoint

Through the native NileDesk API, this operation is `POST /ProcessItem` (base URL `https://app.niledesk.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-process-item-forward.md) for the provider-specific parameters and requirements.

