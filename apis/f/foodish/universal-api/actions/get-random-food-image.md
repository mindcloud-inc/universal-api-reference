# Foodish: Get Random Food Image



```
GET https://connect.mindcloud.co/v1/universal/foodish/latest/actions/get-random-food-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Foodish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foodish/latest/actions/get-random-food-image?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/foodish/latest/actions/get-random-food-image?${params}`, {
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

Through the native Foodish API, this operation is `GET /api/` (base URL `https://foodish-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-food-image.md) for the provider-specific parameters and requirements.

