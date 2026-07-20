# Nexiopay: Update card token



```
PUT https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/update-card-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/update-card-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/update-card-token', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardToken` | string | yes | Saved card token to update. |
| `card` | object | no | Updated card information object documented by Nexio. |
| `data` | object | no | Updated token metadata object documented by Nexio. |
| `shouldUpdateCard` | boolean | no | Whether Nexio should update card details for the token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardType": "string",
      "lastFour": "string",
      "merchantId": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardType` | string | Card brand/type. |
| `lastFour` | string | Last four card digits. |
| `merchantId` | string | Nexio merchant ID. |
| `token` | string | Saved card token. |

## Native endpoint

Through the native Nexiopay API, this operation is `PUT /pay/v3/vault/card/{cardToken}` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-card-token.md) for the provider-specific parameters and requirements.

