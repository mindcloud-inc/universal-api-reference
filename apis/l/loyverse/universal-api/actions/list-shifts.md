# Loyverse: List Shifts

Retrieves shift records from the Loyverse account.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-shifts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-shifts?${params}`, {
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
| `storeIds` | string | no | A comma-separated list of store ids to filter shifts |
| `createdAtMin` | date | no | Show shifts opened after date (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `createdAtMax` | date | no | Show shifts opened before date (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `limit` | number | no | Used for pagination |
| `cursor` | string | no | Used for pagination |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "shifts": [
        {
          "actualCash": 1,
          "cashMovements": [
            {
              "comment": "string",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "employeeId": "string",
              "moneyAmount": 1,
              "type": "string"
            }
          ],
          "cashPayments": 1,
          "cashRefunds": 1,
          "closedAt": "2026-05-07T12:00:00.000Z",
          "closedByEmployee": "string",
          "discounts": 1,
          "expectedCash": 1,
          "grossSales": 1,
          "id": "string",
          "netSales": 1,
          "openedAt": "2026-05-07T12:00:00.000Z",
          "openedByEmployee": "string",
          "paidIn": 1,
          "paidOut": 1,
          "payments": [
            {
              "moneyAmount": 1,
              "paymentTypeId": "string"
            }
          ],
          "posDeviceId": "string",
          "refunds": 1,
          "startingCash": 1,
          "storeId": "string",
          "surcharge": 1,
          "taxes": [
            {
              "moneyAmount": 1,
              "taxId": "string"
            }
          ],
          "tip": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `shifts` | array<object> |  |
| `shifts[].actualCash` | number | The actual money amount at the end of the shift |
| `shifts[].cashMovements` | array<object> | The list of shift cash movements |
| `shifts[].cashMovements[].comment` | string | The description of the cash movement |
| `shifts[].cashMovements[].createdAt` | date | The time when this cash movement was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `shifts[].cashMovements[].employeeId` | string | The employee id who made the cash movement |
| `shifts[].cashMovements[].moneyAmount` | number | The money amount. The value is always positive. |
| `shifts[].cashMovements[].type` | string | The type of cash movement |
| `shifts[].cashPayments` | number | The total money amount of cash payments for the shift |
| `shifts[].cashRefunds` | number | The total money amount of cash refunds for the shift |
| `shifts[].closedAt` | date | The time when the shift was closed |
| `shifts[].closedByEmployee` | string | The employee id who closed the shift |
| `shifts[].discounts` | number | The total money amount of discounts for the shift. The value is always positive. |
| `shifts[].expectedCash` | number | The expected money amount at the end of the shift |
| `shifts[].grossSales` | number | The gross money amount for the shift. It calculates as sum of all payments before discounts but after taxes with type INCLUDED. |
| `shifts[].id` | string |  |
| `shifts[].netSales` | number | The net money amount for the shift. It calculates as gross sales minus discounts and refunds |
| `shifts[].openedAt` | date | The time when the shift was opened |
| `shifts[].openedByEmployee` | string | The employee id who opened the shift |
| `shifts[].paidIn` | number | The money amount added to the cash drawer. |
| `shifts[].paidOut` | number | The money amount removed from the cash drawer. The value is always positive. |
| `shifts[].payments` | array<object> | The list of total money amounts for every payment type in the shift |
| `shifts[].payments[].moneyAmount` | number | The total money amount for the payment type |
| `shifts[].payments[].paymentTypeId` | string |  |
| `shifts[].posDeviceId` | string | The pos device id associated with the shift |
| `shifts[].refunds` | number | The total money amount of refunds for the shift |
| `shifts[].startingCash` | number | The initial money amount at the start of the shift |
| `shifts[].storeId` | string | The store id associated with the shift |
| `shifts[].surcharge` | number | The total money amount of surcharge for the shift. Surcharge is available only for some payment types. |
| `shifts[].taxes` | array<object> | The list of taxes and it's totals for the shift |
| `shifts[].taxes[].moneyAmount` | number | The total money amount for the tax in the shift |
| `shifts[].taxes[].taxId` | string |  |
| `shifts[].tip` | number | The total money amount of tips for the shift. Tips are available only for some payment types. |

## Native endpoint

Through the native Loyverse API, this operation is `GET /shifts` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-shifts.md) for the provider-specific parameters and requirements.

