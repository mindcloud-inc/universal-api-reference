# G2: Browse Product Buyer Intent

Retrieves buyer intent interactions for a product in G2.

```
GET https://connect.mindcloud.co/v1/universal/g2/latest/actions/browse-product-buyer-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a G2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/g2/latest/actions/browse-product-buyer-intent?connectionId=$CONNECTION_ID&limit=25&offset=0&subjectProductId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "subjectProductId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/g2/latest/actions/browse-product-buyer-intent?${params}`, {
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
| `dimensions` | string | no | Comma-separated list of buyer intent dimensions. |
| `measures` | string | no | Comma-separated list of buyer intent measures. |
| `sort` | string | no | Sort field with optional leading minus for descending order. |
| `subjectProductId` | string | yes | Product UUID for scoped buyer intent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "categoryId": "string",
        "categorySlug": "string",
        "companyCount": 1,
        "companyDomain": "string",
        "companyId": "string",
        "companyIntentScore": 1,
        "companyName": "Ava Chen",
        "companyState": "string",
        "day": "string",
        "productId": "string",
        "productSlug": "string",
        "signalType": "string",
        "subjectProductId": "string",
        "subjectProductSlug": "string",
        "totalActivity": 1,
        "visitorCount": 1,
        "visitorId": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.categoryId` | string |  |
| `attributes.categorySlug` | string |  |
| `attributes.companyCount` | number |  |
| `attributes.companyDomain` | string |  |
| `attributes.companyId` | string |  |
| `attributes.companyIntentScore` | number |  |
| `attributes.companyName` | string |  |
| `attributes.companyState` | string |  |
| `attributes.day` | string |  |
| `attributes.productId` | string |  |
| `attributes.productSlug` | string |  |
| `attributes.signalType` | string |  |
| `attributes.subjectProductId` | string |  |
| `attributes.subjectProductSlug` | string |  |
| `attributes.totalActivity` | number |  |
| `attributes.visitorCount` | number |  |
| `attributes.visitorId` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native G2 API, this operation is `GET /api/v2/products/:subject_product_id/buyer_intent` (base URL `https://data.g2.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/browse-product-buyer-intent.md) for the provider-specific parameters and requirements.

