# MILKEE: Create Invoice

Creates a new invoice in MILKEE.

```
POST https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MILKEE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "4640",
  "customerId": 1,
  "positions": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "4640",
    "customerId": 1,
    "positions": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | The numeric MILKEE company ID used in the request path. Default: `4640`. |
| `customerId` | number | yes | Customer ID for the invoice. |
| `date` | string | no | Invoice date. |
| `lang` | string | no | Document language: de, en, fr, or it. |
| `payableUntil` | string | no | Invoice due date. |
| `positions` | string | yes | Invoice positions as a JSON string. |
| `remarks` | string | no | Bottom remarks. |
| `taxRateId` | number | no | Tax rate ID. |
| `title` | string | no | Invoice title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native MILKEE API, this operation is `POST /companies/:companyId/invoices` (base URL `https://app.milkee.ch/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

