# Zoho Invoice: List Customer Payments

Retrieves customer payments from Zoho Invoice.

```
GET https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-customer-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-customer-payments?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/list-customer-payments?${params}`, {
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
| `customerName` | string | no | Search payments by customer name. Variants: customer_name_startswith and customer_name_contains. Maximum length [100] |
| `referenceNumber` | string | no | Search payments by reference number. Variants: reference_number_startswith and reference_number_contains. Maximum length [100] |
| `date` | date | no | Date on which payment is made. Date format yyyy-mm-dd. |
| `amount` | number | no | Search payments by payment amount. Variants: amount_less_than, amount_less_equals, amount_greater_than, amount_greater_equals. |
| `notes` | string | no | Search payments by customer notes. Variants: notes_startswith and notes_contains. |
| `paymentMode` | string | no | Search payments by payment mode. Variants: payment_mode_startswith and payment_mode_contains. |
| `filterBy` | string | no | Filter payments by mode. One of: `options`. |
| `searchText` | string | no | Search payments by reference number, customer name, or payment description. Maximum length [100] |

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

Through the native Zoho Invoice API, this operation is `GET /customerpayments` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-payments.md) for the provider-specific parameters and requirements.

