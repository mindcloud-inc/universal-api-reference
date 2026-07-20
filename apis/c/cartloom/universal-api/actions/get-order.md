# Cartloom: Get Order

Retrieves an order from Cartloom by invoice number.

```
GET https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cartloom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/get-order?connectionId=$CONNECTION_ID&invoice=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoice": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/get-order?${params}`, {
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
| `invoice` | string | yes | Invoice number of the order. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Customer email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "invoice": "string",
      "status": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Order date. |
| `email` | string | Customer email address. |
| `invoice` | string | Order invoice number. |
| `status` | string | Order status. |
| `total` | string | Order total. |

## Native endpoint

Through the native Cartloom API, this operation is `POST /orders/get/format/json` (base URL `https://mindcloudstage0424.cartloom.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

