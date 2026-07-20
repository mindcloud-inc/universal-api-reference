# Ticket Tailor: Get Store

Retrieves store information from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/get-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/get-store?connectionId=$CONNECTION_ID&storeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/get-store?${params}`, {
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
| `storeId` | string | yes | Ticket Tailor store ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "paymentMethods": [
        "string"
      ],
      "products": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | The currency code used by the store |
| `id` | string | A unique identifier for the store |
| `name` | string | Name of the store |
| `object` | string |  |
| `paymentMethods` | array<string> | Array of payment method IDs associated with the store |
| `products` | array<string> | Array of product IDs that are sold in the store |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/stores/:store_id` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-store.md) for the provider-specific parameters and requirements.

