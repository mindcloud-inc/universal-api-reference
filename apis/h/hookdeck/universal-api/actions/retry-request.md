# Hookdeck: Retry Request

Retries a request in Hookdeck.

```
PUT https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/retry-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/retry-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/retry-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Hookdeck request ID from the `id` path parameter. |
| `body` | object | yes | JSON request body for retrying a Hookdeck request. Use an empty object to consider all connection IDs, or provide `webhook_ids`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {}
      ],
      "request": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> | Events created by the retry operation, when present. |
| `request` | object | Retried Hookdeck request. |

## Native endpoint

Through the native Hookdeck API, this operation is `POST /requests/:id/retry` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retry-request.md) for the provider-specific parameters and requirements.

