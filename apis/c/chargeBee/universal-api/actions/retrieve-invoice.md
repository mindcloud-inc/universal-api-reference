# ChargeBee: Retrieve Invoice

Retrieves an invoice from ChargeBee.

```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-invoice?connectionId=$CONNECTION_ID&invoice_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoice_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-invoice?${params}`, {
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
| `invoice_id` | string | yes | The Chargebee invoice identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency_code": "string",
      "customer_id": "string",
      "date": 1,
      "id": "string",
      "object": "string",
      "status": "string",
      "subscription_id": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency_code` | string |  |
| `customer_id` | string |  |
| `date` | number |  |
| `id` | string |  |
| `object` | string |  |
| `status` | string |  |
| `subscription_id` | string |  |
| `total` | number |  |

## Native endpoint

Through the native ChargeBee API, this operation is `GET invoices/:invoice_id` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-invoice.md) for the provider-specific parameters and requirements.

