# Rentman: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-invoice?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-invoice?${params}`, {
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
| `id` | number | yes | Numeric Rentman invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_manager": "string",
      "contact": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "customer": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "date_sent": "2026-05-07T12:00:00.000Z",
      "days_after_expiry": 1,
      "displayname": "Ava Chen",
      "expiration": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "final_payment_reminder_sent": "2026-05-07T12:00:00.000Z",
      "finalized": true,
      "from_project": true,
      "id": 1,
      "integration_reference_id": "string",
      "invoicetype": "string",
      "is_paid": true,
      "modified": "2026-05-07T12:00:00.000Z",
      "number": "string",
      "outstanding_balance": 1,
      "payment_date": "2026-05-07T12:00:00.000Z",
      "payment_reminder_sent": 1,
      "price": 1,
      "price_invat": 1,
      "procent": 1,
      "project": "string",
      "project_crew_price": 1,
      "project_insurance_price": 1,
      "project_other_price": 1,
      "project_rental_price": 1,
      "project_sale_price": 1,
      "project_total_price": 1,
      "project_total_price_cancelled": 1,
      "project_transport_price": 1,
      "subject": "string",
      "sum_factuurregels": 1,
      "tags": "string",
      "total_paid": 1,
      "updateHash": "string",
      "vat_amount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_manager` | string |  |
| `contact` | string |  |
| `created` | date |  |
| `creator` | string |  |
| `customer` | string |  |
| `date` | date |  |
| `date_sent` | date |  |
| `days_after_expiry` | number |  |
| `displayname` | string |  |
| `expiration` | date |  |
| `filename` | string |  |
| `final_payment_reminder_sent` | date |  |
| `finalized` | boolean |  |
| `from_project` | boolean |  |
| `id` | number |  |
| `integration_reference_id` | string |  |
| `invoicetype` | string |  |
| `is_paid` | boolean |  |
| `modified` | date |  |
| `number` | string |  |
| `outstanding_balance` | number |  |
| `payment_date` | date |  |
| `payment_reminder_sent` | number |  |
| `price` | number |  |
| `price_invat` | number |  |
| `procent` | number |  |
| `project` | string |  |
| `project_crew_price` | number |  |
| `project_insurance_price` | number |  |
| `project_other_price` | number |  |
| `project_rental_price` | number |  |
| `project_sale_price` | number |  |
| `project_total_price` | number |  |
| `project_total_price_cancelled` | number |  |
| `project_transport_price` | number |  |
| `subject` | string |  |
| `sum_factuurregels` | number |  |
| `tags` | string |  |
| `total_paid` | number |  |
| `updateHash` | string |  |
| `vat_amount` | number |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /invoices/:id` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

