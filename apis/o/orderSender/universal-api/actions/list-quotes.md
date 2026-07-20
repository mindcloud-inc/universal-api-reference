# Order Sender: List Quotes

Retrieves sales quotes from Order Sender.

```
GET https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-quotes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-quotes?${params}`, {
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
      "CL_codice": "string",
      "CL_nome": "string",
      "codice": "string",
      "codice_ordine": "string",
      "data_invio": "string",
      "descrizione": "string",
      "id": "string",
      "numero": "string",
      "prezzo": "string",
      "quantita": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CL_codice` | string |  |
| `CL_nome` | string |  |
| `codice` | string |  |
| `codice_ordine` | string |  |
| `data_invio` | string |  |
| `descrizione` | string |  |
| `id` | string |  |
| `numero` | string |  |
| `prezzo` | string |  |
| `quantita` | string |  |

## Native endpoint

Through the native Order Sender API, this operation is `GET /op/export/res/preventivi` (base URL `https://business.ordersender.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-quotes.md) for the provider-specific parameters and requirements.

