# SearchApi: Get Product Specs



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-product-specs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-product-specs?connectionId=$CONNECTION_ID&productId=10300376706158921238" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "10300376706158921238"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-product-specs?${params}`, {
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
| `productId` | string | yes | Google Shopping product ID. Example: `10300376706158921238`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "specifications": [
        {}
      ],
      "topInsights": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `specifications` | array<object> |  |
| `topInsights` | array<object> |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-specs.md) for the provider-specific parameters and requirements.

