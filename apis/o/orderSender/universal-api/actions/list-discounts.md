# Order Sender: List Discounts

Retrieves discount records from Order Sender.

```
GET https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-discounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-discounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-discounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "categoria_merceologica": "string",
      "codice_cliente": "string",
      "codice_fornitore": "string",
      "codice_prodotto": "string",
      "prezzo_netto": 1,
      "sconto1": 1,
      "sconto2": 1,
      "sconto3": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoria_merceologica` | string | Product category code. |
| `codice_cliente` | string | Customer code. |
| `codice_fornitore` | string | Supplier code. |
| `codice_prodotto` | string | Product code. |
| `prezzo_netto` | number | Net price. |
| `sconto1` | number | Discount 1. |
| `sconto2` | number | Discount 2. |
| `sconto3` | number | Discount 3. |

## Native endpoint

Through the native Order Sender API, this operation is `GET /op/export/res/sconti` (base URL `https://business.ordersender.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-discounts.md) for the provider-specific parameters and requirements.

