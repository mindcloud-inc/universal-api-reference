# Conveyor: List Product Lines

Retrieves product lines for a program from Conveyor.

```
GET https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-product-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-product-lines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-product-lines?${params}`, {
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
      "_embedded": {
        "product_lines": [
          {
            "id": "string",
            "name": "Ava Chen"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded` | object |  |
| `_embedded.product_lines` | array<object> |  |
| `_embedded.product_lines[].id` | string |  |
| `_embedded.product_lines[].name` | string |  |

## Native endpoint

Through the native Conveyor API, this operation is `GET /v2/product_lines` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-product-lines.md) for the provider-specific parameters and requirements.

