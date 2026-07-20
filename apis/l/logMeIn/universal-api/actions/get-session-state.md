# LogMeIn: Get Session State

Retrieves a support session state from LogMeIn.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-session-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-session-state?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-session-state?${params}`, {
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
| `sessionId` | string | yes | Required session ID to retrieve. |

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
      "status": "string"
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

## Native endpoint

Through the native LogMeIn API, this operation is `GET /goto-resolve/v1/sessions/:sessionId` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-state.md) for the provider-specific parameters and requirements.

