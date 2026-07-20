# Bridge: Create Payment Consent

Creates a payment consent in Bridge.

```
POST https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payment-consent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payment-consent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalReference": "string",
  "redirectUrl": "https://example.com",
  "transactions[]": [
    {}
  ],
  "user.email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridge/latest/actions/create-payment-consent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalReference": "string",
    "redirectUrl": "https://example.com",
    "transactions[]": [{}],
    "transactions[]": [{}],
    "user.email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalReference` | string | yes | A reference to your payment |
| `redirectUrl` | string | yes | URL to redirect the user after consent completion |
| `transactions[]` | array<object> | yes | Details of the payment that requires consent |
| `transactions[]` | array<object> | yes | Details of the payment that requires consent |
| `user.email` | string | yes | Mandatory |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user.firstName` | string | no | Mandatory with lastname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.lastName` | string | no | Mandatory with firstname or only company_name (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |
| `user.companyName` | string | no | Mandatory or firstname and last_name must be completed (max 35 char : alphanumeric, space and some symbols + ( ) / . - ! ? , ; & % € are supported but it must contain at least one letter) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "consentUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `consentUrl` | string | The URL on Bridge Pay to accept the terms and conditions |

## Native endpoint

Through the native Bridge API, this operation is `POST /payment/consents` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-consent.md) for the provider-specific parameters and requirements.

