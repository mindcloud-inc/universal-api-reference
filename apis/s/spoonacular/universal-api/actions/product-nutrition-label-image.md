# Spoonacular: Product Nutrition Label Image

Retrieves a product nutrition label image from Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/product-nutrition-label-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/product-nutrition-label-image?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/product-nutrition-label-image?${params}`, {
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
| `id` | string | yes | Required by the Spoonacular endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "image": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `image` | string |  |

## Native endpoint

Through the native Spoonacular API, this operation is `GET /food/products/{id}/nutritionLabel.png` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/product-nutrition-label-image.md) for the provider-specific parameters and requirements.

