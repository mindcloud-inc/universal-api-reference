# LogMeIn: Create Support Session

Creates a new support session in LogMeIn.

```
POST https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-support-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-support-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-support-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerName` | string | yes | Required customer name for the support session. |
| `sessionType` | number | no | Optional numeric session type. |
| `supportType` | number | no | Optional numeric support type. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhooks[]` | array<object> | no | Optional webhook subscription entries for session updates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerName": "Ava Chen",
      "id": "string",
      "sessionId": "string",
      "state": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerName` | string |  |
| `id` | string |  |
| `sessionId` | string |  |
| `state` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `POST /goto-resolve/v1/sessions` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-support-session.md) for the provider-specific parameters and requirements.

