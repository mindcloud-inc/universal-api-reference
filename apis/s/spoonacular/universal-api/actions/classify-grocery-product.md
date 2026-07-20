# Spoonacular: Classify Grocery Product

Classifies a grocery product with Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/classify-grocery-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/classify-grocery-product?connectionId=$CONNECTION_ID&requestBody=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestBody": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/classify-grocery-product?${params}`, {
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
| `requestBody` | string | yes | The required request body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native Spoonacular API, this operation is `POST /food/products/classify` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/classify-grocery-product.md) for the provider-specific parameters and requirements.

