# Nexiopay: Save echeck token



```
POST https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/save-echeck-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/save-echeck-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "token": "string",
  "bank": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/save-echeck-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "token": "string",
    "bank": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `token` | string | yes | One-time-use token returned by the token endpoint. |
| `bank` | object | yes | Bank account information object documented by Nexio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bank": {},
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
| `bank` | object | Saved bank metadata. |
| `data` | object | Additional response data. |
| `merchantId` | string | Nexio merchant ID. |
| `token` | object | Saved echeck token object. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/saveECheck` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-echeck-token.md) for the provider-specific parameters and requirements.

