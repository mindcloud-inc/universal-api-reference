# Zoho Inventory: Get Invoice

Retrieves an invoice from Zoho Inventory.

```
GET https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=string&organizationId=%7B%7Bcredentials.organizationId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "string",
  "organizationId": "{{credentials.organizationId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | string | yes | The Zoho Inventory invoice_id for the invoice. |
| `organizationId` | string | yes | Zoho Inventory organization ID to run this request against. Default: `{{credentials.organizationId}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "created_time": "string",
      "customer_id": "string",
      "customer_name": "Ava Chen",
      "date": "string",
      "due_date": "string",
      "invoice_id": "string",
      "invoice_number": "string",
      "last_modified_time": "string",
      "line_items": [
        {}
      ],
      "notes": "string",
      "reference_number": "string",
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `created_time` | string |  |
| `customer_id` | string |  |
| `customer_name` | string |  |
| `date` | string |  |
| `due_date` | string |  |
| `invoice_id` | string |  |
| `invoice_number` | string |  |
| `last_modified_time` | string |  |
| `line_items` | array<object> |  |
| `notes` | string |  |
| `reference_number` | string |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Zoho Inventory API, this operation is `GET /invoices/:invoice_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/inventory/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

