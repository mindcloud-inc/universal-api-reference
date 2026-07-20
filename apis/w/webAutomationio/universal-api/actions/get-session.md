# WebAutomation.io: Get Session

Gets details for a specific extractor session.

```
GET https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/get-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebAutomation.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/get-session?connectionId=$CONNECTION_ID&sessionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/get-session?${params}`, {
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
| `sessionId` | number | yes | The session ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebAutomation.io API returns.

## Native endpoint

Through the native WebAutomation.io API, this operation is `GET /sessions/{{SESSIONID}}/` (base URL `https://webautomation.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session.md) for the provider-specific parameters and requirements.

