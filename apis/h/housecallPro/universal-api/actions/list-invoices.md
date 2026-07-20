# Housecall Pro: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-invoices?${params}`, {
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
| `status` | list<string> | no | Filter invoices by status. One of: `canceled`, `open`, `paid`, `pending_payment`, `uncollectible`, `voided`. Accepts multiple values as an array. |
| `customerUuid[]` | array<string> | no | Filter invoices by customer UUIDs. Accepts multiple values as an array. Example: `cus_ccdcb54ddb5a42bea9466d386a637af8`. |
| `paymentMethod` | list<string> | no | Filter invoices by payment method. One of: `ach`, `consumer_financing`, `credit_card`, `external`, `mobile_check_deposit`. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationIds[]` | array<string> | no | Filter invoices by location ids. Accepts multiple values as an array. Example: `loc_123`. |
| `createdAtMin` | date | no | Filter invoices created on or after this timestamp. Example: `2024-01-30T00:00:00Z`. |
| `createdAtMax` | date | no | Filter invoices created on or before this timestamp. Example: `2024-01-30T00:00:00Z`. |
| `dueAtMin` | date | no | Filter invoices due on or after this timestamp. Example: `2024-01-30T00:00:00Z`. |
| `dueAtMax` | date | no | Filter invoices due on or before this timestamp. Example: `2024-01-30T00:00:00Z`. |
| `paidAtMin` | date | no | Filter invoices paid on or after this timestamp. Example: `2024-01-30T00:00:00Z`. |
| `paidAtMax` | date | no | Filter invoices paid on or before this timestamp. Example: `2024-01-30T00:00:00Z`. |
| `amountDueMin` | number | no | Filter invoices with due amount at or above this value. Example: `10`. |
| `amountDueMax` | number | no | Filter invoices with due amount at or below this value. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "discounts": [
        {}
      ],
      "displayDueConcept": "string",
      "dueAmount": 1,
      "dueAt": "string",
      "dueConcept": "string",
      "id": "string",
      "invoiceDate": "string",
      "invoiceNumber": "string",
      "items": [
        {}
      ],
      "paidAt": "string",
      "payments": [
        {}
      ],
      "sentAt": "string",
      "serviceDate": "string",
      "status": "string",
      "subtotal": 1,
      "taxes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Invoice total amount. |
| `discounts` | array<object> | Invoice discounts. |
| `displayDueConcept` | string | Human-readable due concept. |
| `dueAmount` | number | Outstanding invoice balance. |
| `dueAt` | string | Invoice due timestamp. |
| `dueConcept` | string | Provider due concept token. |
| `id` | string | Invoice UUID. |
| `invoiceDate` | string | Invoice date. |
| `invoiceNumber` | string | Invoice number. |
| `items` | array<object> | Invoice items. |
| `paidAt` | string | Paid timestamp. |
| `payments` | array<object> | Invoice payments. |
| `sentAt` | string | Sent timestamp. |
| `serviceDate` | string | Service date. |
| `status` | string | Invoice status. |
| `subtotal` | number | Invoice subtotal amount. |
| `taxes` | array<object> | Invoice taxes. |

## Native endpoint

Through the native Housecall Pro API, this operation is `GET /invoices` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

