# lc.cx: Create Short Link

Creates a new short link in lc.cx.

```
POST https://connect.mindcloud.co/v1/universal/lccx/latest/actions/create-short-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lc.cx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lccx/latest/actions/create-short-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destination": "string",
  "domainId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lccx/latest/actions/create-short-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destination": "string",
    "domainId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destination` | string | yes | The destination URL for the new shortlink. |
| `domainId` | string | yes | The domain ID to use for the new shortlink. |
| `customPath` | string | no | An optional custom path for the shortlink. |
| `tagIds[]` | array<string> | no | Optional tag IDs to attach to the shortlink. |
| `note` | string | no | An optional note stored on the shortlink. |
| `rule` | string | no | An optional lc.cx rule value for the shortlink. |
| `expirationTimestamp` | number | no | An optional UNIX timestamp after which the shortlink expires. |
| `expirationUrl` | string | no | An optional URL to use after the shortlink expires. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native lc.cx API returns.

## Native endpoint

Through the native lc.cx API, this operation is `POST /shorten` (base URL `https://api.lc.cx/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-short-link.md) for the provider-specific parameters and requirements.

