# Foodish: Get Food Image by Category



```
GET https://connect.mindcloud.co/v1/universal/foodish/latest/actions/get-food-image-by-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Foodish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foodish/latest/actions/get-food-image-by-category?connectionId=$CONNECTION_ID&category=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/foodish/latest/actions/get-food-image-by-category?${params}`, {
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
| `category` | string | yes | Foodish food category. The provider documents category availability on its demo site. |

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
| `image` | string | URL of the selected food image. |

## Native endpoint

Through the native Foodish API, this operation is `GET /api/images/:category` (base URL `https://foodish-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-food-image-by-category.md) for the provider-specific parameters and requirements.

