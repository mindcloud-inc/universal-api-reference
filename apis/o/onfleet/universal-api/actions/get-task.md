# Onfleet: Get Task

Retrieves a task from Onfleet.

```
GET https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | The Onfleet task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completeAfter": 1,
      "completeBefore": 1,
      "container": {},
      "destination": {},
      "id": "string",
      "notes": "string",
      "pickupTask": true,
      "quantity": 1,
      "recipients": [
        {}
      ],
      "serviceTime": 1,
      "shortId": "string",
      "state": 1,
      "trackingURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completeAfter` | number |  |
| `completeBefore` | number |  |
| `container` | object |  |
| `destination` | object |  |
| `id` | string |  |
| `notes` | string |  |
| `pickupTask` | boolean |  |
| `quantity` | number |  |
| `recipients` | array<object> |  |
| `serviceTime` | number |  |
| `shortId` | string |  |
| `state` | number |  |
| `trackingURL` | string |  |

## Native endpoint

Through the native Onfleet API, this operation is `GET /tasks/:taskId` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

