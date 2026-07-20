# Merit: Create Payment Of Sales Offer



```
POST https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-payment-of-sales-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-payment-of-sales-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerName": "Ava Chen",
  "offerNo": "string",
  "paymentDate": "202604221800",
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-payment-of-sales-offer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerName": "Ava Chen",
    "offerNo": "string",
    "paymentDate": "202604221800",
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerName` | string | yes |  |
| `offerNo` | string | yes |  |
| `paymentDate` | string | yes | Example: `202604221800`. |
| `amount` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bankId` | string | no |  |
| `iban` | string | no |  |
| `refNo` | string | no |  |
| `currencyCode` | string | no |  |
| `currencyRate` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merit API returns.

## Native endpoint

Through the native Merit API, this operation is `POST v2/sendPaymentO` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-of-sales-offer.md) for the provider-specific parameters and requirements.

