# Reepay: Get Charge

Retrieves a charge from Reepay.

```
GET https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-charge?connectionId=$CONNECTION_ID&handle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-charge?${params}`, {
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
| `handle` | string | yes | Charge handle from Reepay. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": "string",
      "handle": "string",
      "order_lines": [
        {
          "amount": 1,
          "ordertext": "string",
          "quantity": 1,
          "vat": 1
        }
      ],
      "refunded_amount": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `created` | date |  |
| `currency` | string |  |
| `customer` | string |  |
| `handle` | string |  |
| `order_lines[].amount` | number |  |
| `order_lines[].ordertext` | string |  |
| `order_lines[].quantity` | number |  |
| `order_lines[].vat` | number |  |
| `refunded_amount` | number |  |
| `state` | string |  |

## Native endpoint

Through the native Reepay API, this operation is `GET /v1/charge/:handle` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-charge.md) for the provider-specific parameters and requirements.

