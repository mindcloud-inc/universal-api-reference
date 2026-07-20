# Pastebin: Generate User Session Key

Creates a Pastebin user session key.

```
POST https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/generate-user-session-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pastebin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/generate-user-session-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "memberUsername": "Ava Chen",
  "memberPassword": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/generate-user-session-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "memberUsername": "Ava Chen",
    "memberPassword": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `memberUsername` | string | yes | Pastebin username used to generate an api_user_key. |
| `memberPassword` | string | yes | Pastebin password used to generate an api_user_key. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pastebin API returns.

## Native endpoint

Through the native Pastebin API, this operation is `POST /api_login.php` (base URL `https://pastebin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-user-session-key.md) for the provider-specific parameters and requirements.

