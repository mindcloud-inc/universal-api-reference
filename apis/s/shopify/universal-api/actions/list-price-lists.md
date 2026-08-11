# Shopify: List Price Lists



```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-price-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-price-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-price-lists?${params}`, {
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
      "catalog": {
        "id": "string",
        "title": "string"
      },
      "currency": "string",
      "fixedPricesCount": 1,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `catalog.id` | string | Associated catalog GID |
| `catalog.title` | string | Associated catalog title |
| `currency` | string | Price list currency |
| `fixedPricesCount` | number | Number of fixed prices |
| `id` | string | Shopify price list GID |
| `name` | string | Price list name |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-07/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-price-lists.md) for the provider-specific parameters and requirements.

