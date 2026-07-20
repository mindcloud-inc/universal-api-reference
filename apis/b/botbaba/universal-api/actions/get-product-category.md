# Botbaba: Get Product Category



```
GET https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-product-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botbaba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-product-category?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-product-category?${params}`, {
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
| `id` | number | yes | The product category identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": 1,
      "botName": "Ava Chen",
      "categoryName": "Ava Chen",
      "description": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | number |  |
| `botName` | string |  |
| `categoryName` | string |  |
| `description` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Botbaba API, this operation is `GET /api/GetProductCategoryById` (base URL `https://app.botbaba.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-category.md) for the provider-specific parameters and requirements.

