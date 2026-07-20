# Unleashed: List Stock On Hand

Retrieves stock-on-hand records from your Unleashed account.

```
GET https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-stock-on-hand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-stock-on-hand?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-stock-on-hand?${params}`, {
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
      "allocatedQty": 1,
      "availableQty": 1,
      "avgCost": 1,
      "daysSinceLastSale": 1,
      "guid": "string",
      "lastModifiedOn": "string",
      "onPurchase": 1,
      "productCode": "string",
      "productDescription": "string",
      "productGroupName": "Ava Chen",
      "productGuid": "string",
      "qtyOnHand": 1,
      "totalCost": 1,
      "warehouseCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocatedQty` | number |  |
| `availableQty` | number |  |
| `avgCost` | number |  |
| `daysSinceLastSale` | number |  |
| `guid` | string |  |
| `lastModifiedOn` | string |  |
| `onPurchase` | number |  |
| `productCode` | string |  |
| `productDescription` | string |  |
| `productGroupName` | string |  |
| `productGuid` | string |  |
| `qtyOnHand` | number |  |
| `totalCost` | number |  |
| `warehouseCode` | string |  |

## Native endpoint

Through the native Unleashed API, this operation is `GET /StockOnHand/:pageNumber` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stock-on-hand.md) for the provider-specific parameters and requirements.

