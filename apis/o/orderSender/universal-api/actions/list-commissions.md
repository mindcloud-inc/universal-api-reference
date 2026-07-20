# Order Sender: List Commissions

Retrieves commission records from Order Sender.

```
GET https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-commissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-commissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-commissions?${params}`, {
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
      "codice_fornitore": "string",
      "codice_prodotto": "string",
      "provvigione": 1,
      "soglia": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoria_merceologica` | string |  |
| `codice_fornitore` | string |  |
| `codice_prodotto` | string |  |
| `provvigione` | number |  |
| `soglia` | number |  |

## Native endpoint

Through the native Order Sender API, this operation is `GET /op/export/res/provvigioni` (base URL `https://business.ordersender.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-commissions.md) for the provider-specific parameters and requirements.

