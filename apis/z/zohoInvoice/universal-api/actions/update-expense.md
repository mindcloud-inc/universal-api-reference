# Zoho Invoice: Update Expense

Updates an expense in Zoho Invoice.

```
PUT https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "917578947",
  "expenseId": "982000000030049",
  "amount": "120.5",
  "referenceNumber": "#EXP-20260312-001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-expense', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "917578947",
    "expenseId": "982000000030049",
    "amount": "120.5",
    "referenceNumber": "#EXP-20260312-001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | list<string> | yes | ID of the organization header X-com-zoho-invoice-organizationid. Example: `917578947`. |
| `expenseId` | string | yes | Unique identifier of the expense. Example: `982000000030049`. |
| `amount` | number | yes | Total expense value. Example: `120.5`. |
| `referenceNumber` | string | yes | Reference number of the expense. Example: `#EXP-20260312-001`. |
| `date` | date | no | Date of the expense. Example: `2026-03-12`. |
| `description` | string | no | Description of the expense. Example: `Updated taxi receipt`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | no | ID of the expense account. Example: `982000000561057`. |
| `isBillable` | boolean | no | Check if an expense is billable. |
| `customerId` | string | no | ID of the expense account. Example: `982000000567001`. |
| `projectId` | string | no | ID of the project associated with the customer. Example: `982000000567226`. |

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

Through the native Zoho Invoice API, this operation is `PUT /expenses/:expense_id` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-expense.md) for the provider-specific parameters and requirements.

