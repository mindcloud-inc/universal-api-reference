# Nexiopay: Create one-time-use token



```
POST https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/create-one-time-use-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/create-one-time-use-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/create-one-time-use-token', {
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
| `data` | object | no | Transaction and customer data object documented by Nexio. |
| `card` | object | no | Card information object documented by Nexio. |
| `bank` | object | no | Bank account information object documented by Nexio. |
| `processingOptions` | object | no | Processing options object documented by Nexio. |
| `uiOptions` | object | no | Iframe UI options object documented by Nexio. |
| `paymentMethod` | string | no | Payment method selector documented by Nexio. |
| `shouldUpdateCard` | boolean | no | Whether Nexio should update an existing card token. |
| `isAuthOnly` | boolean | no | Whether to create the token for an auth-only transaction. |
| `installment` | object | no | Installment data object documented by Nexio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "expiration": "2026-05-07T12:00:00.000Z",
      "fraudUrl": "https://example.com",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Tokenized transaction data. |
| `expiration` | date | Token expiration timestamp. |
| `fraudUrl` | string | Fraud/device collection URL when returned. |
| `token` | string | One-time-use token. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/token` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-one-time-use-token.md) for the provider-specific parameters and requirements.

