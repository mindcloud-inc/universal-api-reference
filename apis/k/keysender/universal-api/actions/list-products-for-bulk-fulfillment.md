# Keysender: List Products For Bulk Fulfillment

Retrieves products from Keysender for bulk fulfillment.

```
GET https://connect.mindcloud.co/v1/universal/keysender/latest/actions/list-products-for-bulk-fulfillment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/list-products-for-bulk-fulfillment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keysender/latest/actions/list-products-for-bulk-fulfillment?${params}`, {
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
      "docs": [
        {}
      ],
      "itemsPerPage": 1,
      "page": 1,
      "total": 1,
      "totalAll": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs` | array<object> | Catalog products returned for the current page. |
| `itemsPerPage` | number | Number of products returned per page. |
| `page` | number | Current result page. |
| `total` | number | Total number of products in the current result set. |
| `totalAll` | number | Total number of products across the catalog. |

## Native endpoint

Through the native Keysender API, this operation is `GET /catalog/products` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products-for-bulk-fulfillment.md) for the provider-specific parameters and requirements.

