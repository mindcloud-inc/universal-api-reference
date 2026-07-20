# Nexiopay: Save card token



```
POST https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/save-card-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/save-card-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "token": "string",
  "card": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/save-card-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "token": "string",
    "card": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `token` | string | yes | One-time-use token returned by the token endpoint. |
| `card` | object | yes | Card information object documented by Nexio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card": {},
      "data": {},
      "merchantId": "string",
      "token": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card` | object | Saved card metadata. |
| `data` | object | Additional response data. |
| `merchantId` | string | Nexio merchant ID. |
| `token` | object | Saved card token object. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/saveCard` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-card-token.md) for the provider-specific parameters and requirements.

