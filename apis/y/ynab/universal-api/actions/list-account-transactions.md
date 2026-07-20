# YNAB: List Account Transactions

Retrieves transactions for an account in YNAB.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-account-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-account-transactions?connectionId=$CONNECTION_ID&planId=string&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string",
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-account-transactions?${params}`, {
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
| `planId` | string | yes |  |
| `accountId` | string | yes |  |
| `sinceDate` | date | no |  |
| `type` | string | no |  |
| `lastKnowledgeOfServer` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountName": "Ava Chen",
      "amount": 1,
      "amountFormatted": "string",
      "approved": true,
      "categoryName": "Ava Chen",
      "cleared": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "deleted": true,
      "id": "string",
      "payeeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountName` | string | The account name. |
| `amount` | number | The transaction amount in milliunits. |
| `amountFormatted` | string | The transaction amount formatted for display. |
| `approved` | boolean | Whether the transaction is approved. |
| `categoryName` | string | The category name when present. |
| `cleared` | string | The cleared status. |
| `date` | date | The transaction date. |
| `deleted` | boolean | Whether the transaction has been deleted. |
| `id` | string | The YNAB transaction ID. |
| `payeeName` | string | The payee name when present. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans/:planId/accounts/:accountId/transactions` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-transactions.md) for the provider-specific parameters and requirements.

