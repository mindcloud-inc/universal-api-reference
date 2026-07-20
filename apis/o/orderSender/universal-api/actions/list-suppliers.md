# Order Sender: List Suppliers

Retrieves supplier records from Order Sender.

```
GET https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-suppliers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-suppliers?${params}`, {
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
| `delimiter` | string | no | Delimiter used only when requesting CSV output. |
| `format` | string | no | Response format. Use json for structured records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codice": "string",
      "email": "ava@example.com",
      "nome": "string",
      "partitaiva": "string",
      "telefono": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codice` | string |  |
| `email` | string |  |
| `nome` | string |  |
| `partitaiva` | string |  |
| `telefono` | string |  |

## Native endpoint

Through the native Order Sender API, this operation is `GET /op/export/res/fornitori` (base URL `https://business.ordersender.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

