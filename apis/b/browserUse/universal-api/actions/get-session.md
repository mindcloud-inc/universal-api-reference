# Browser Use: Get Session

Retrieves a session from Browser Use.

```
GET https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-session?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-session?${params}`, {
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
| `sessionId` | string | yes | Browser Use session ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isTaskSuccessful": true,
      "liveUrl": "https://example.com",
      "model": "string",
      "output": {},
      "status": "string",
      "stepCount": 1,
      "title": "string",
      "totalCostUsd": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `isTaskSuccessful` | boolean |  |
| `liveUrl` | string |  |
| `model` | string |  |
| `output` | object |  |
| `status` | string |  |
| `stepCount` | number |  |
| `title` | string |  |
| `totalCostUsd` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Browser Use API, this operation is `GET /sessions/:session_id` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session.md) for the provider-specific parameters and requirements.

