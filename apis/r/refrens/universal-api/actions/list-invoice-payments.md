# Refrens: List Invoice Payments



```
GET https://connect.mindcloud.co/v1/universal/refrens/latest/actions/list-invoice-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/list-invoice-payments?connectionId=$CONNECTION_ID&invoice=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoice": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refrens/latest/actions/list-invoice-payments?${params}`, {
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
| `invoice` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "payments": [
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
| `payments` | array<object> |  |

## Native endpoint

Through the native Refrens API, this operation is `GET /businesses/:urlKey/invoices/:invoice/payments` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoice-payments.md) for the provider-specific parameters and requirements.

