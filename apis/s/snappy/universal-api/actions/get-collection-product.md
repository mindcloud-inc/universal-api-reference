# Snappy: Get Collection Product

Retrieves a product from a specific Snappy collection.

```
GET https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-collection-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snappy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-collection-product?connectionId=$CONNECTION_ID&collectionId=string&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string",
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-collection-product?${params}`, {
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
| `collectionId` | string | yes | Collection ID. |
| `productId` | string | yes | Product ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `minBudget` | number | no | Minimum budget. |
| `maxBudget` | number | no | Maximum budget. |
| `companyId` | string | no | Company ID. |
| `country` | string | no | Country. Default: `US`. |
| `accountId` | string | no | Account ID. |
| `fields[]` | array<string> | no | Additional product fields to include. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snappy API returns.

## Native endpoint

Through the native Snappy API, this operation is `GET /collections/{collectionId}/products/{productId}` (base URL `https://api.snappy.com/public-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection-product.md) for the provider-specific parameters and requirements.

