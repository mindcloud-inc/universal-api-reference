# Payrexx: Create Gateway

Creates a gateway in Payrexx.

```
POST https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-gateway
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-gateway" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": "1000",
  "currency": "CHF"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-gateway', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": "1000",
    "currency": "CHF"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Amount of payment in cents. Example: `1000`. |
| `currency` | string | yes | Currency of payment (ISO code). Example: `CHF`. |
| `purpose` | string | no | The purpose of the payment. Example: `MindCloud Payrexx gateway test`. |
| `referenceId` | string | no | An internal reference id used by your system. Example: `mc-gateway-001`. |
| `preAuthorization` | boolean | no | Whether charge payment manually at a later date (type authorization). Example: `false`. |
| `reservation` | boolean | no | Whether charge payment manually at a later date (type reservation). Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "applicationFee": 1,
      "createdAt": 1,
      "currency": "string",
      "hash": "string",
      "id": 1,
      "language": "string",
      "link": "https://example.com",
      "preAuthorization": true,
      "referenceId": "string",
      "requestId": 1,
      "sku": {},
      "status": "string",
      "vatRate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `applicationFee` | number |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `hash` | string |  |
| `id` | number |  |
| `language` | string |  |
| `link` | string |  |
| `preAuthorization` | boolean |  |
| `referenceId` | string |  |
| `requestId` | number |  |
| `sku` | object |  |
| `status` | string |  |
| `vatRate` | number |  |

## Native endpoint

Through the native Payrexx API, this operation is `POST Gateway/` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-gateway.md) for the provider-specific parameters and requirements.

