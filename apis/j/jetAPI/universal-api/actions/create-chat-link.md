# JetAPI: Create Chat Link

Creates a new chat link in JetAPI.

```
POST https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/create-chat-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JetAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/create-chat-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/create-chat-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authType` | number | no | 0 requires password entry, 1 disables password entry. Default: `0`. |
| `password` | string | no | Password for logging into iframe chat when auth_type=0. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": "https://example.com",
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string | Direct iframe chat link. |
| `meta` | object | Response metadata. |

## Native endpoint

Through the native JetAPI API, this operation is `POST /api/v1/chatter/` (base URL `https://api.jetapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat-link.md) for the provider-specific parameters and requirements.

