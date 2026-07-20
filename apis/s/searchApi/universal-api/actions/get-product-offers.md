# SearchApi: Get Product Offers



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-product-offers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-product-offers?connectionId=$CONNECTION_ID&productId=1974369455608953604" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1974369455608953604"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-product-offers?${params}`, {
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
| `productId` | string | yes | Google Shopping product ID. Example: `1974369455608953604`. |
| `productToken` | string | no | Google Shopping product token. Optional when Product ID is provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "offers": [
        {}
      ],
      "pagination": {},
      "product": {},
      "searchInformation": {},
      "searchMetadata": {},
      "searchParameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `offers` | array<object> |  |
| `pagination` | object |  |
| `product` | object |  |
| `searchInformation` | object |  |
| `searchMetadata` | object |  |
| `searchParameters` | object |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-offers.md) for the provider-specific parameters and requirements.

