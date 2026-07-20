# Extensiv Order Manager: List Product Listings

Retrieves product listings from Extensiv Order Manager.

```
GET https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-product-listings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extensiv Order Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-product-listings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-product-listings?${params}`, {
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
| `active` | boolean | no |  |
| `createdDateFrom` | string | no |  |
| `createdDateTo` | string | no |  |
| `listingId[]` | array<number> | no |  |
| `listingSku[]` | array<string> | no |  |
| `masterSku[]` | array<string> | no |  |
| `modifiedDateFrom` | string | no |  |
| `modifiedDateTo` | string | no |  |
| `productId[]` | array | no |  |
| `salesChannelId` | string | no |  |
| `warehouseId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "listingId": 1,
      "listingSku": "string",
      "masterSku": "string",
      "productId": 1,
      "salesChannelId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the listing is active. |
| `listingId` | number | Product listing identifier. |
| `listingSku` | string | Listing SKU. |
| `masterSku` | string | Master SKU. |
| `productId` | number | Product identifier. |
| `salesChannelId` | number | Sales channel identifier. |

## Native endpoint

Through the native Extensiv Order Manager API, this operation is `GET /v1/listings` (base URL `https://api.skubana.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-product-listings.md) for the provider-specific parameters and requirements.

