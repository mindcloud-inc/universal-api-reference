# Walmart: Search Seller Catalog

Search your seller catalog with optional filters like Price, Listing Status, Rating etc.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/search-seller-catalog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/search-seller-catalog?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/search-seller-catalog?${params}`, {
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
| `filters[].field` | list<string> | no | Pick a field to filter by. |
| `query` | object | no |  |
| `query.field` | list<string> | no | Choose a specific field to search. |
| `sort.field` | list<string> | no | Pick a field to sort by. |
| `filters[]` | array<object> | no |  |
| `query.value` | string | no | The value you want to search for. |
| `sort.order` | list<string> | no | Allowed: `ASC`, `DESC` |
| `filters[].op` | list<string> | no | Allowed: `equals`, `between`, `greater_than`, `less_than` |
| `sort` | object | no | Sort the results by a specific field. |
| `filters[].values` | string | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": "string",
      "gtin": "string",
      "itemId": "string",
      "lifecycleStatus": "string",
      "manufacturer": "string",
      "mart": "string",
      "price": {
        "amount": "string",
        "unit": "string"
      },
      "productName": "Ava Chen",
      "productType": "string",
      "publishedStatus": {
        "reasons": [
          "string"
        ],
        "status": "string"
      },
      "shelf": [
        "string"
      ],
      "sku": "string",
      "variantGroupId": "string",
      "variantGroupInfo": {
        "groupingAttributes": [
          {
            "name": "Ava Chen",
            "value": "string"
          }
        ],
        "isPrimary": "string"
      },
      "wpid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | string |  |
| `gtin` | string |  |
| `itemId` | string |  |
| `lifecycleStatus` | string |  |
| `manufacturer` | string |  |
| `mart` | string |  |
| `price.amount` | string |  |
| `price.unit` | string |  |
| `productName` | string |  |
| `productType` | string |  |
| `publishedStatus.reasons[]` | string |  |
| `publishedStatus.status` | string |  |
| `shelf[]` | string |  |
| `sku` | string |  |
| `variantGroupId` | string |  |
| `variantGroupInfo.groupingAttributes[].name` | string |  |
| `variantGroupInfo.groupingAttributes[].value` | string |  |
| `variantGroupInfo.isPrimary` | string |  |
| `wpid` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/items/catalog/search` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-seller-catalog.md) for the provider-specific parameters and requirements.

