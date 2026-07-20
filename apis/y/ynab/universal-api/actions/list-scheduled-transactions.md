# YNAB: List Scheduled Transactions

Retrieves scheduled transactions from a YNAB plan.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-scheduled-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-scheduled-transactions?connectionId=$CONNECTION_ID&planId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-scheduled-transactions?${params}`, {
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
| `planId` | string | yes | The id of the plan. You can also use last-used. |
| `lastKnowledgeOfServer` | number | no | Only include entities changed since this server knowledge value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountName": "Ava Chen",
      "amount": 1,
      "amountFormatted": "string",
      "categoryName": "Ava Chen",
      "dateNext": "2026-05-07T12:00:00.000Z",
      "deleted": true,
      "frequency": "string",
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
| `amount` | number | The scheduled transaction amount in milliunits. |
| `amountFormatted` | string | The scheduled transaction amount formatted for display. |
| `categoryName` | string | The category name when present. |
| `dateNext` | date | The next scheduled date. |
| `deleted` | boolean | Whether the scheduled transaction has been deleted. |
| `frequency` | string | The scheduled transaction frequency. |
| `id` | string | The YNAB scheduled transaction ID. |
| `payeeName` | string | The payee name when present. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans/:planId/scheduled_transactions` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scheduled-transactions.md) for the provider-specific parameters and requirements.

