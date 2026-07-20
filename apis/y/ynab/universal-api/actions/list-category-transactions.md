# YNAB: List Category Transactions

Retrieves transactions for a category in YNAB.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-category-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-category-transactions?connectionId=$CONNECTION_ID&planId=string&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string",
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-category-transactions?${params}`, {
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
| `planId` | string | yes | The id of the plan. You can also use last-used or default when enabled. |
| `categoryId` | string | yes | The id of the category. |
| `sinceDate` | date | no | Only include transactions on or after this date. |
| `type` | string | no | Only include transactions of the specified type. |
| `lastKnowledgeOfServer` | number | no | Only include changes since this server knowledge value. |

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
| `accountName` | string | The account name, when present. |
| `amount` | number | The transaction amount in milliunits. |
| `amountFormatted` | string | The formatted transaction amount. |
| `approved` | boolean | Whether the transaction is approved. |
| `categoryName` | string | The category name, when present. |
| `cleared` | string | The transaction cleared state. |
| `date` | date | The transaction date. |
| `deleted` | boolean | Whether the transaction has been deleted. |
| `id` | string | The transaction ID. |
| `payeeName` | string | The payee name, when present. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans/:planId/categories/:categoryId/transactions` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-category-transactions.md) for the provider-specific parameters and requirements.

