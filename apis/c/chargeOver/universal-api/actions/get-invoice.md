# ChargeOver: Get Invoice

Retrieves detailed invoice records from ChargeOver.

```
GET https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeOver `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | number | yes | The ChargeOver invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "customer_id": 1,
      "date": "string",
      "due_date": "string",
      "invoice_id": 1,
      "invoice_status_name": "Ava Chen",
      "is_paid": true,
      "is_void": true,
      "package_id": 1,
      "payments": 1,
      "refnumber": 1,
      "total": 1,
      "url_pdflink": "https://example.com",
      "url_self": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `customer_id` | number |  |
| `date` | string |  |
| `due_date` | string |  |
| `invoice_id` | number |  |
| `invoice_status_name` | string |  |
| `is_paid` | boolean |  |
| `is_void` | boolean |  |
| `package_id` | number |  |
| `payments` | number |  |
| `refnumber` | number |  |
| `total` | number |  |
| `url_pdflink` | string |  |
| `url_self` | string |  |

## Native endpoint

Through the native ChargeOver API, this operation is `GET /invoice/:invoice_id` (base URL `https://{{credentials.siteName}}.chargeover.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

