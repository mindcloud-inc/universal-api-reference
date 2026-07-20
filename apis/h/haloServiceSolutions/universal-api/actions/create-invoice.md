# Halo Service Solutions: Create Invoice

Creates a new invoice in Halo Service Solutions.

```
POST https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `[]` | array<object> | no | Invoice payload array. |
| `[].invoice_date` | string | no | Date invoiced. |
| `[].name` | string | no | Invoice name. |
| `[].client_id` | number | no | Client ID for the invoice. |
| `[].sitenumber` | number | no | Site number for the invoice. |
| `[].uid` | number | no | User ID for the invoice. |
| `[].assigned_agent` | number | no | Assigned agent ID for the invoice. |
| `[].add_salesorder` | number | no | Existing sales order to invoice from. |
| `[].internal_note` | string | no | Internal note for the invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "add_salesorder": 1,
      "amountdue": 1,
      "assigned_agent": 1,
      "client_id": 1,
      "client_name": "Ava Chen",
      "duedate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "internal_note": "string",
      "invoice_date": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "paymentstatus": 1,
      "site_name": "Ava Chen",
      "sitenumber": 1,
      "total": 1,
      "uid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `add_salesorder` | number |  |
| `amountdue` | number |  |
| `assigned_agent` | number |  |
| `client_id` | number |  |
| `client_name` | string |  |
| `duedate` | date |  |
| `id` | number | Invoice ID |
| `internal_note` | string |  |
| `invoice_date` | date |  |
| `name` | string |  |
| `paymentstatus` | number |  |
| `site_name` | string |  |
| `sitenumber` | number |  |
| `total` | number |  |
| `uid` | number |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `POST /Invoice` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

