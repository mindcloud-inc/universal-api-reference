# Walmart: List Items

Retrieve all items from a partner’s catalog.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-items?${params}`, {
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
| `lifecycleStatus` | list<string> | no | The status of an item in the overall lifecycle. |
| `publishedStatus` | list<string> | no | The status of an item in the submission process. |
| `condition` | list<string> | no | The condition of a product. |
| `availability` | list<string> | no | The availability of a product. |
| `showDuplicateItemInfo` | boolean | no | Indicates whether to include details of duplicate items in the response. Set this parameter to true if you want to receive information on duplicate items. |
| `includeCustomerFavoritesStatus` | boolean | no | Toggle on to include isCustomerFavorite item details in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gtin": "string",
      "lifecycleStatus": "string",
      "mart": "string",
      "price": {
        "amount": 1,
        "currency": "string"
      },
      "productName": "Ava Chen",
      "productType": "string",
      "publishedStatus": "string",
      "shelf": "string",
      "sku": "string",
      "upc": "string",
      "wpid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gtin` | string |  |
| `lifecycleStatus` | string |  |
| `mart` | string |  |
| `price.amount` | number |  |
| `price.currency` | string |  |
| `productName` | string |  |
| `productType` | string |  |
| `publishedStatus` | string |  |
| `shelf` | string |  |
| `sku` | string |  |
| `upc` | string |  |
| `wpid` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/items` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

