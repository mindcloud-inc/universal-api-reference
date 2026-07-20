# JVZoo: Get Recurring Payment Status

Retrieves recurring payment status from JVZoo.

```
GET https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-recurring-payment-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JVZoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-recurring-payment-status?connectionId=$CONNECTION_ID&preKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "preKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-recurring-payment-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `preKey` | string | yes | The key used for the recurring payment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "contactEmail": "ava@example.com",
      "created": "2026-05-07T12:00:00.000Z",
      "currentPayments": 1,
      "currentPaymentsAmount": "string",
      "hasPaymentTrial": true,
      "id": 1,
      "ip": "string",
      "lastDate": "2026-05-07T12:00:00.000Z",
      "maxAmountPerPayment": "string",
      "maxNumberOfPayments": 1,
      "maxTotalOfAllPayments": "string",
      "nextDate": "2026-05-07T12:00:00.000Z",
      "nextPayment": "string",
      "paymentCount": 1,
      "paymentFirstPayout": "string",
      "paymentPeriod": 1,
      "paymentTrialPayout": "string",
      "paymentTrialPeriod": 1,
      "paymentTrialPrice": "string",
      "payout": "string",
      "paypalEmail": "ava@example.com",
      "preKey": "string",
      "price": "string",
      "productId": 1,
      "referrer": "string",
      "senderEmail": "ava@example.com",
      "status": "string",
      "tid": "string",
      "vtid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Recurring payment code when available. |
| `contactEmail` | string | Contact email address. |
| `created` | date | When the recurring payment was created. |
| `currentPayments` | number | Number of payments made so far. |
| `currentPaymentsAmount` | string | Current payments total amount. |
| `hasPaymentTrial` | boolean | Whether a trial payment exists. |
| `id` | number | Recurring payment ID. |
| `ip` | string | IP address associated with the payment. |
| `lastDate` | date | Last payment date. |
| `maxAmountPerPayment` | string | Maximum amount per payment. |
| `maxNumberOfPayments` | number | Maximum number of payments. |
| `maxTotalOfAllPayments` | string | Maximum total value of all payments. |
| `nextDate` | date | Next payment date. |
| `nextPayment` | string | Next payment amount. |
| `paymentCount` | number | Payment count. |
| `paymentFirstPayout` | string | First payout amount. |
| `paymentPeriod` | number | Payment period value. |
| `paymentTrialPayout` | string | Trial payout amount. |
| `paymentTrialPeriod` | number | Trial payment period. |
| `paymentTrialPrice` | string | Trial payment price. |
| `payout` | string | Recurring payout value. |
| `paypalEmail` | string | PayPal email address. |
| `preKey` | string | Recurring payment preKey. |
| `price` | string | Recurring payment price. |
| `productId` | number | Product ID. |
| `referrer` | string | Referrer URL. |
| `senderEmail` | string | Sender email address. |
| `status` | string | Recurring payment status. |
| `tid` | string | Transaction ID when available. |
| `vtid` | string | Vendor transaction ID when available. |

## Native endpoint

Through the native JVZoo API, this operation is `GET /recurring_payment/:preKey` (base URL `https://api.jvzoo.com/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recurring-payment-status.md) for the provider-specific parameters and requirements.

