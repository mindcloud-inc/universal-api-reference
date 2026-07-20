# Order Sender: List Prospects

Retrieves prospect records from Order Sender.

```
GET https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-prospects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderSender/latest/actions/list-prospects?${params}`, {
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
      "citta": "string",
      "codice": "string",
      "email": "ava@example.com",
      "nome": "string",
      "ragione_sociale": "string",
      "telefono": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `citta` | string |  |
| `codice` | string |  |
| `email` | string |  |
| `nome` | string |  |
| `ragione_sociale` | string |  |
| `telefono` | string |  |

## Native endpoint

Through the native Order Sender API, this operation is `GET /op/export/res/prospect` (base URL `https://business.ordersender.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-prospects.md) for the provider-specific parameters and requirements.

