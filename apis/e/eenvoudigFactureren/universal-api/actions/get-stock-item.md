# EenvoudigFactureren: Get Stock Item

Retrieves a stock item from EenvoudigFactureren.

```
GET https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-stock-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EenvoudigFactureren `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-stock-item?connectionId=$CONNECTION_ID&stockitem_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stockitem_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-stock-item?${params}`, {
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
| `stockitem_id` | string | yes | EenvoudigFactureren stock item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "name": "Ava Chen",
      "price": 1,
      "stockitem_id": 1,
      "uri": "string",
      "vat": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `name` | string |  |
| `price` | number |  |
| `stockitem_id` | number |  |
| `uri` | string |  |
| `vat` | number |  |

## Native endpoint

Through the native EenvoudigFactureren API, this operation is `GET /stockitems/:stockitem_id` (base URL `https://eenvoudigfactureren.be/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stock-item.md) for the provider-specific parameters and requirements.

