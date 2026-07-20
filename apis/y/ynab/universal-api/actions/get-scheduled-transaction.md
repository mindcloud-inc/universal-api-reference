# YNAB: Get Scheduled Transaction

Retrieves a scheduled transaction from a YNAB plan.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-scheduled-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-scheduled-transaction?connectionId=$CONNECTION_ID&planId=string&scheduledTransactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string",
  "scheduledTransactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/get-scheduled-transaction?${params}`, {
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
| `scheduledTransactionId` | string | yes | The id of the scheduled transaction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "accountName": "Ava Chen",
      "amount": 1,
      "amountCurrency": 1,
      "amountFormatted": "string",
      "categoryId": "string",
      "categoryName": "Ava Chen",
      "dateFirst": "2026-05-07T12:00:00.000Z",
      "dateNext": "2026-05-07T12:00:00.000Z",
      "deleted": true,
      "flagColor": "string",
      "flagName": "Ava Chen",
      "frequency": "string",
      "id": "string",
      "memo": "string",
      "payeeId": "string",
      "payeeName": "Ava Chen",
      "subtransactions": [
        {}
      ],
      "transferAccountId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | The source account ID. |
| `accountName` | string | The account name. |
| `amount` | number | The scheduled transaction amount in milliunits. |
| `amountCurrency` | number | The currency-adjusted scheduled transaction amount. |
| `amountFormatted` | string | The formatted scheduled transaction amount. |
| `categoryId` | string | The category ID, when present. |
| `categoryName` | string | The category name, when present. |
| `dateFirst` | date | The first scheduled date. |
| `dateNext` | date | The next scheduled date. |
| `deleted` | boolean | Whether the scheduled transaction has been deleted. |
| `flagColor` | string | The scheduled transaction flag color, when present. |
| `flagName` | string | The scheduled transaction flag name, when present. |
| `frequency` | string | The scheduled transaction frequency. |
| `id` | string | The scheduled transaction ID. |
| `memo` | string | The scheduled transaction memo, when present. |
| `payeeId` | string | The payee ID, when present. |
| `payeeName` | string | The payee name, when present. |
| `subtransactions` | array<object> | The scheduled subtransactions. |
| `transferAccountId` | string | The transfer account ID, when present. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans/:planId/scheduled_transactions/:scheduledTransactionId` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scheduled-transaction.md) for the provider-specific parameters and requirements.

