# BrowserStack: Set Session Status

Updates a session status in BrowserStack Automate.

```
PUT https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/set-session-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrowserStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/set-session-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string",
  "status": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserStack/latest/actions/set-session-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string",
    "status": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | BrowserStack hashed session ID. |
| `status` | string | yes | BrowserStack session outcome: passed or failed. One of: `0`, `1`. |
| `reason` | string | no | Reason text, typically used when marking a session failed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BrowserStack API returns.

## Native endpoint

Through the native BrowserStack API, this operation is `PUT /automate/sessions/:session_id.json` (base URL `https://api.browserstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-session-status.md) for the provider-specific parameters and requirements.

