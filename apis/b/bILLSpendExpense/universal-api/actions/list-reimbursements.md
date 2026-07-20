# BILL Spend & Expense: List Reimbursements

Retrieves reimbursements from BILL Spend & Expense.

```
GET https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-reimbursements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Spend & Expense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-reimbursements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-reimbursements?${params}`, {
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
| `filters` | string | no | Filter expression documented by BILL for this list endpoint. |
| `max` | number | no | Maximum number of results to return. |
| `nextPage` | string | no | Next page token returned by the previous list response. |
| `prevPage` | string | no | Previous page token returned by the previous list response. |
| `sort` | string | no | Sort expression documented by BILL for this list endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "budgetId": "string",
      "budgetUuid": "string",
      "fundRequestAmount": 1,
      "fundRequestBudgetAmount": 1,
      "id": "string",
      "merchantName": "Ava Chen",
      "note": "string",
      "occurredDate": "string",
      "receipts": [
        {
          "filename": "Ava Chen",
          "uuid": "string"
        }
      ],
      "retired": true,
      "status": "string",
      "statusHistory": [
        {
          "actorId": "string",
          "actorRole": "string",
          "note": "string",
          "occurredTime": "string",
          "status": "string"
        }
      ],
      "submittedTime": "string",
      "type": "string",
      "userId": "string",
      "userUuid": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `budgetId` | string |  |
| `budgetUuid` | string |  |
| `fundRequestAmount` | number |  |
| `fundRequestBudgetAmount` | number |  |
| `id` | string |  |
| `merchantName` | string |  |
| `note` | string |  |
| `occurredDate` | string |  |
| `receipts[].filename` | string |  |
| `receipts[].uuid` | string |  |
| `retired` | boolean |  |
| `status` | string |  |
| `statusHistory[].actorId` | string |  |
| `statusHistory[].actorRole` | string |  |
| `statusHistory[].note` | string |  |
| `statusHistory[].occurredTime` | string |  |
| `statusHistory[].status` | string |  |
| `submittedTime` | string |  |
| `type` | string |  |
| `userId` | string |  |
| `userUuid` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native BILL Spend & Expense API, this operation is `GET spend/reimbursements` (base URL `https://gateway.{{credentials.environment}}.bill.com/connect/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reimbursements.md) for the provider-specific parameters and requirements.

