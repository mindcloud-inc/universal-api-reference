# Bridge: Create Payment Link

Creates a payment link in Bridge.

```
POST https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payment-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactions[]": [{}],
    "transactions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactions[]` | array<object> | yes | Details of the payment |
| `transactions[]` | array<object> | yes | Details of the payment |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user.firstName` | string | no | Mandatory with lastname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.lastName` | string | no | Mandatory with firstname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.companyName` | string | no | Mandatory or firstname and last_name must be completed (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.email` | string | no | Mandatory depending on your use case |
| `user.externalReference` | string | no | We recommend filling this value with a unique ID that identifies your user. It helps Bridge optimize fraud detection by tracking how many payments have been initiated by a single user within a specific period. |
| `expiredDate` | date | no | The link status will be set to "EXPIRED" after this date. Format is yyyy-MM-ddThh:mm:ssZ (ISO8601) |
| `clientReference` | string | no | A reference to link this link to your system (100 char. max) |
| `callbackUrl` | string | no | If you want to redirect the users to your interface instead of Bridge's interface after they completed the journey from their bank website or application |
| `country` | string | no | To define the default banks displayed in the banks list. If not defined, french banks will be displayed. |
| `providerId` | number | no | If the parameter is set, your user won't see the providers list. Be careful to select providers with at least the single_payment capability |

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
| `id` | string | The created payment link's unique identifier |
| `url` | string | The url to go to initiate the payment |

## Native endpoint

Through the native Bridge API, this operation is `POST /payment/payment-links` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-link.md) for the provider-specific parameters and requirements.

