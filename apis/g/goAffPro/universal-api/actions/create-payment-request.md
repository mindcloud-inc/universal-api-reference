# GoAffPro: Create Payment Request

Creates a new payment request in GoAffPro.

```
POST https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/create-payment-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/create-payment-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "affiliateId": 1,
  "txIds[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/create-payment-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "affiliateId": 1,
    "txIds[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `affiliateId` | number | yes | ID of the affiliate making the payment request. |
| `txIds[]` | array<number> | yes | Transaction IDs to include in the payment request. |
| `note` | string | no | Optional note for the payment request. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceUrl` | string | no | Optional invoice URL for the payment request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "id": 1,
      "note": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Total amount of the payment request. |
| `id` | number | ID of the created payment request. |
| `note` | string | Note for the payment request. |

## Native endpoint

Through the native GoAffPro API, this operation is `POST /admin/payments/requests` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-request.md) for the provider-specific parameters and requirements.

