# Bridge: Create Payment Request

Creates a payment request in Bridge.

```
POST https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payment-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payment-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "callbackUrl": "https://example.com",
  "transactions[]": [
    {}
  ],
  "providerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payment-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "callbackUrl": "https://example.com",
    "transactions[]": [{}],
    "transactions[]": [{}],
    "providerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | yes | The user will be redirected to this URL after the payment |
| `transactions[]` | array<object> | yes |  |
| `transactions[]` | array<object> | yes |  |
| `providerId` | number | yes | The unique identifier of the user's provider |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user.firstName` | string | no | Mandatory with lastname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.lastName` | string | no | Mandatory with firstname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.companyName` | string | no | Mandatory or firstname and last_name must be completed (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.email` | string | no | Mandatory depending on your use case |
| `user.externalReference` | string | no | We recommend filling this value with a unique ID that identifies your user. It helps Bridge optimize fraud detection by tracking how many payments have been initiated by a single user within a specific period. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The created payment request's unique identifier |
| `url` | string | The url to go to initiate the payment |

## Native endpoint

Through the native Bridge API, this operation is `POST /payment/payment-requests` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-request.md) for the provider-specific parameters and requirements.

