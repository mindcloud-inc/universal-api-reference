# Zoho Invoice: Get Expense

Retrieves an expense from Zoho Invoice.

```
GET https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/get-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/get-expense?connectionId=$CONNECTION_ID&organizationId=917578947&expenseId=982000000030049" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "917578947",
  "expenseId": "982000000030049"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/get-expense?${params}`, {
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
| `organizationId` | list<string> | yes | ID of the organization header X-com-zoho-invoice-organizationid. Example: `917578947`. |
| `expenseId` | string | yes | Unique identifier of the expense. Example: `982000000030049`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountName": "Ava Chen",
      "amount": 1,
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "expenseId": "string",
      "isBillable": true,
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "referenceNumber": "string",
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `accountName` | string |  |
| `amount` | number |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `date` | date |  |
| `description` | string |  |
| `expenseId` | string |  |
| `isBillable` | boolean |  |
| `lastModifiedTime` | date |  |
| `referenceNumber` | string |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `GET /expenses/:expense_id` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-expense.md) for the provider-specific parameters and requirements.

