# Gelato: Stock Availability

Retrieves regional stock availability for Gelato products.

```
GET https://connect.mindcloud.co/v1/universal/gelato/latest/actions/stock-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gelato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/stock-availability?connectionId=$CONNECTION_ID&products%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "products[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gelato/latest/actions/stock-availability?${params}`, {
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
| `products[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "productsAvailability": [
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
| `productsAvailability` | array<object> | Per-product stock region availability returned by Gelato. |

## Native endpoint

Through the native Gelato API, this operation is `POST https://product.gelatoapis.com/v3/stock/region-availability` (base URL `https://order.gelatoapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stock-availability.md) for the provider-specific parameters and requirements.

