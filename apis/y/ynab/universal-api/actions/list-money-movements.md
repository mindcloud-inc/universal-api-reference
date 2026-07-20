# YNAB: List Money Movements

Retrieves money movements from a YNAB plan.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-money-movements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-money-movements?connectionId=$CONNECTION_ID&planId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-money-movements?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountCurrency": 1,
      "amountFormatted": "string",
      "fromCategoryId": "string",
      "id": "string",
      "moneyMovementGroupId": "string",
      "month": "2026-05-07T12:00:00.000Z",
      "movedAt": "2026-05-07T12:00:00.000Z",
      "note": "string",
      "performedByUserId": "string",
      "toCategoryId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | The money movement amount in milliunits. |
| `amountCurrency` | number | The currency-adjusted money movement amount. |
| `amountFormatted` | string | The formatted money movement amount. |
| `fromCategoryId` | string | The source category ID, when present. |
| `id` | string | The money movement ID. |
| `moneyMovementGroupId` | string | The money movement group ID, when present. |
| `month` | date | The money movement month, when present. |
| `movedAt` | date | When the money movement was processed on the server, when present. |
| `note` | string | The money movement note, when present. |
| `performedByUserId` | string | The user who performed the money movement, when present. |
| `toCategoryId` | string | The destination category ID, when present. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans/:planId/money_movements` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-money-movements.md) for the provider-specific parameters and requirements.

