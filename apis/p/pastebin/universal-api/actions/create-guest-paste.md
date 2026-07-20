# Pastebin: Create Guest Paste

Creates a guest paste in Pastebin.

```
POST https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/create-guest-paste
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pastebin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/create-guest-paste" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pasteContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/create-guest-paste', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pasteContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pasteContent` | string | yes | The text content to include in the Pastebin paste. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pastebin API returns.

## Native endpoint

Through the native Pastebin API, this operation is `POST /api_post.php` (base URL `https://pastebin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-guest-paste.md) for the provider-specific parameters and requirements.

