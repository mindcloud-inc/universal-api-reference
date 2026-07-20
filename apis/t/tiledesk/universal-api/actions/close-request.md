# Tiledesk: Close Request

Closes a request in the current Tiledesk project.

```
PUT https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/close-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiledesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/close-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/close-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | The request identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "closed_at": "string",
      "request_id": "string",
      "status": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `closed_at` | string |  |
| `request_id` | string |  |
| `status` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Tiledesk API, this operation is `PUT /{{credentials.projectId}}/requests/:requestId/close` (base URL `https://api.tiledesk.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/close-request.md) for the provider-specific parameters and requirements.

