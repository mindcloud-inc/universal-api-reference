# Shopper Approved: Get Product Aggregate Statistics

Retrieves product aggregate statistics from Shopper Approved.

```
GET https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-product-aggregate-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopper Approved `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-product-aggregate-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-product-aggregate-statistics?${params}`, {
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
| `byMatchKey` | boolean | no | Whether to group product aggregates by a matching key like SKU or MPN. |
| `siteOnly` | boolean | no | Whether to return only the site_totals object. |
| `fastMode` | boolean | no | Whether to use the optimized fastmode query. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "productTotals": {},
      "siteTotals": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `productTotals` | object |  |
| `siteTotals` | object |  |

## Native endpoint

Through the native Shopper Approved API, this operation is `GET /aggregates/products/:siteid` (base URL `https://api.shopperapproved.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-aggregate-statistics.md) for the provider-specific parameters and requirements.

