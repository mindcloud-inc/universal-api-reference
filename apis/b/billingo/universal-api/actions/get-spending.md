# Billingo: Get Spending

Retrieves a spending record from Billingo.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-spending
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-spending?connectionId=$CONNECTION_ID&id=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-spending?${params}`, {
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
| `id` | number | yes | Billingo spending ID from the path. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "currency": "string",
      "due_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "invoice_date": "2026-05-07T12:00:00.000Z",
      "invoice_number": "string",
      "organization_id": 1,
      "partner": {},
      "payment_method": "string",
      "total_gross": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `currency` | string |  |
| `due_date` | date |  |
| `id` | number |  |
| `invoice_date` | date |  |
| `invoice_number` | string |  |
| `organization_id` | number |  |
| `partner` | object |  |
| `payment_method` | string |  |
| `total_gross` | number |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /spendings/:id` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-spending.md) for the provider-specific parameters and requirements.

