# Order Sender: List Orders

Retrieves sales orders from Order Sender.

```
GET https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-orders?${params}`, {
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
| `dateFrom` | string | no | Export start date in YYYY-MM-DD format. |
| `dateTo` | string | no | Export end date in YYYY-MM-DD format. |
| `delimiter` | string | no | Delimiter used only when requesting CSV output. |
| `format` | string | no | Response format. Use json for structured records. |
| `fornitore` | string | no | Optional supplier code filter. |
| `ids` | string | no | Optional comma-separated order numbers filter. |
| `NumOrdFrom` | string | no | Optional start order number filter. |
| `NumOrdTo` | string | no | Optional end order number filter. |

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

Through the native Order Sender API, this operation is `GET /op/export/res/ordini` (base URL `https://business.ordersender.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

