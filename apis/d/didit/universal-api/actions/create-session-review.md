# Didit: Create Session Review

Creates a new review for a session in Didit.

```
POST https://connect.mindcloud.co/v1/universal/didit/latest/actions/create-session-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Didit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/didit/latest/actions/create-session-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/didit/latest/actions/create-session-review', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Didit session identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "newStatus": "string",
      "note": "string",
      "oldStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `newStatus` | string |  |
| `note` | string |  |
| `oldStatus` | string |  |

## Native endpoint

Through the native Didit API, this operation is `POST /sessions/{sessionId}/reviews/` (base URL `https://verification.didit.me/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session-review.md) for the provider-specific parameters and requirements.

