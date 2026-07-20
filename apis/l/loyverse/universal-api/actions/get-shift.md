# Loyverse: Get Shift

Retrieves a shift record from Loyverse.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-shift?connectionId=$CONNECTION_ID&shiftId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shiftId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-shift?${params}`, {
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
| `shiftId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualCash` | number | The actual money amount at the end of the shift |
| `cashMovements` | array<object> | The list of shift cash movements |
| `cashMovements[].comment` | string | The description of the cash movement |
| `cashMovements[].createdAt` | date | The time when this cash movement was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `cashMovements[].employeeId` | string | The employee id who made the cash movement |
| `cashMovements[].moneyAmount` | number | The money amount. The value is always positive. |
| `cashMovements[].type` | string | The type of cash movement |
| `cashPayments` | number | The total money amount of cash payments for the shift |
| `cashRefunds` | number | The total money amount of cash refunds for the shift |
| `closedAt` | date | The time when the shift was closed |
| `closedByEmployee` | string | The employee id who closed the shift |
| `discounts` | number | The total money amount of discounts for the shift. The value is always positive. |
| `expectedCash` | number | The expected money amount at the end of the shift |
| `grossSales` | number | The gross money amount for the shift. It calculates as sum of all payments before discounts but after taxes with type INCLUDED. |
| `id` | string |  |
| `netSales` | number | The net money amount for the shift. It calculates as gross sales minus discounts and refunds |
| `openedAt` | date | The time when the shift was opened |
| `openedByEmployee` | string | The employee id who opened the shift |
| `paidIn` | number | The money amount added to the cash drawer. |
| `paidOut` | number | The money amount removed from the cash drawer. The value is always positive. |
| `payments` | array<object> | The list of total money amounts for every payment type in the shift |
| `payments[].moneyAmount` | number | The total money amount for the payment type |
| `payments[].paymentTypeId` | string |  |
| `posDeviceId` | string | The pos device id associated with the shift |
| `refunds` | number | The total money amount of refunds for the shift |
| `startingCash` | number | The initial money amount at the start of the shift |
| `storeId` | string | The store id associated with the shift |
| `surcharge` | number | The total money amount of surcharge for the shift. Surcharge is available only for some payment types. |
| `taxes` | array<object> | The list of taxes and it's totals for the shift |
| `taxes[].moneyAmount` | number | The total money amount for the tax in the shift |
| `taxes[].taxId` | string |  |
| `tip` | number | The total money amount of tips for the shift. Tips are available only for some payment types. |

## Native endpoint

Through the native Loyverse API, this operation is `GET /shifts/:shift_id` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shift.md) for the provider-specific parameters and requirements.

