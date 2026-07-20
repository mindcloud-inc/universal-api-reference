# Zoho Invoice: Retrieve Payment

Retrieves a payment from Zoho Invoice.

```
GET https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/retrieve-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/retrieve-payment?connectionId=$CONNECTION_ID&organizationId=string&paymentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "paymentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/retrieve-payment?${params}`, {
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
| `organizationId` | list<string> | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `paymentId` | string | yes | Unique identifier of the payment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "customerId": "string",
      "customerName": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "paymentId": "string",
      "paymentMode": "string",
      "paymentNumber": "string",
      "paymentStatus": "string",
      "referenceNumber": "string",
      "unusedAmount": 1,
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `customerId` | string |  |
| `customerName` | string |  |
| `date` | date |  |
| `paymentId` | string |  |
| `paymentMode` | string |  |
| `paymentNumber` | string |  |
| `paymentStatus` | string |  |
| `referenceNumber` | string |  |
| `unusedAmount` | number |  |
| `updatedTime` | date |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `GET /customerpayments/:payment_id` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-payment.md) for the provider-specific parameters and requirements.

