# Didit: List Session Reviews

Retrieves reviews for a session from Didit.

```
GET https://connect.mindcloud.co/v1/universal/didit/latest/actions/list-session-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Didit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/didit/latest/actions/list-session-reviews?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/didit/latest/actions/list-session-reviews?${params}`, {
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

Through the native Didit API, this operation is `GET /sessions/{sessionId}/reviews/` (base URL `https://verification.didit.me/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-session-reviews.md) for the provider-specific parameters and requirements.

