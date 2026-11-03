# Rithum for Brands: List Sites



```
GET https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-sites?${params}`, {
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
      "adjustmentReasons": [
        {
          "code": 1,
          "description": "string"
        }
      ],
      "cancellationConfiguration": {
        "supportsOrderCancellations": true,
        "supportsOrderItemCancellations": true,
        "supportsOrderItemRMACancellations": true
      },
      "id": 1,
      "refundConfiguration": {
        "supportsOrderItemRefunds": true,
        "supportsOrderItemRMARefunds": true,
        "supportsOrderRefunds": true
      },
      "siteCategoryID": 1,
      "siteCategoryName": "Ava Chen",
      "siteName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adjustmentReasons[].code` | number |  |
| `adjustmentReasons[].description` | string |  |
| `cancellationConfiguration.supportsOrderCancellations` | boolean |  |
| `cancellationConfiguration.supportsOrderItemCancellations` | boolean |  |
| `cancellationConfiguration.supportsOrderItemRMACancellations` | boolean |  |
| `id` | number |  |
| `refundConfiguration.supportsOrderItemRefunds` | boolean |  |
| `refundConfiguration.supportsOrderItemRMARefunds` | boolean |  |
| `refundConfiguration.supportsOrderRefunds` | boolean |  |
| `siteCategoryID` | number |  |
| `siteCategoryName` | string |  |
| `siteName` | string |  |

## Native endpoint

Through the native Rithum for Brands API, this operation is `GET Sites` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

