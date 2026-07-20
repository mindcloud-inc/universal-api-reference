# Spoonacular Food: Classify Food Image by URL

Classifies a food image in Spoonacular Food by URL.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/classify-food-image-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/classify-food-image-by-url?connectionId=$CONNECTION_ID&imageUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/classify-food-image-by-url?${params}`, {
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
| `imageUrl` | string | yes | Public URL of the food image to classify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "probability": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `probability` | number |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /food/images/classify` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/classify-food-image-by-url.md) for the provider-specific parameters and requirements.

