# ERPLY Books: Get Points of Sale

Retrieves points of sale from ERPLY Books.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-points-of-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-points-of-sale?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-points-of-sale?${params}`, {
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
      "records": [
        {
          "added": 1,
          "address": "string",
          "defaultCustomerID": 1,
          "geoLatitude": "string",
          "geoLongitude": "string",
          "lastCouponNo": 1,
          "lastInvoiceNo": "string",
          "lastModified": 1,
          "name": "Ava Chen",
          "paymentServiceProvider": "string",
          "phone": "string",
          "pointOfSaleID": 1,
          "printSalesPersonName": 1,
          "receiptWidth": "string",
          "shopName": "Ava Chen",
          "storeCreditEnabled": 1,
          "storeHours": "string",
          "type": {},
          "vatrate": {},
          "vatrateID": 1,
          "vatrateIDrange1": 1,
          "vatrateIDrange2": 1,
          "vatSumRange1": 1,
          "vatSumRange2": 1,
          "warehouseID": 1,
          "warehouseName": "Ava Chen"
        }
      ],
      "status": {
        "errorCode": 1,
        "generationTime": 1,
        "recordsInResponse": 1,
        "recordsTotal": 1,
        "request": "string",
        "requestUnixTime": 1,
        "responseStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records[].added` | number |  |
| `records[].address` | string |  |
| `records[].defaultCustomerID` | number |  |
| `records[].geoLatitude` | string |  |
| `records[].geoLongitude` | string |  |
| `records[].lastCouponNo` | number |  |
| `records[].lastInvoiceNo` | string |  |
| `records[].lastModified` | number |  |
| `records[].name` | string |  |
| `records[].paymentServiceProvider` | string |  |
| `records[].phone` | string |  |
| `records[].pointOfSaleID` | number |  |
| `records[].printSalesPersonName` | number |  |
| `records[].receiptWidth` | string |  |
| `records[].shopName` | string |  |
| `records[].storeCreditEnabled` | number |  |
| `records[].storeHours` | string |  |
| `records[].type` | object |  |
| `records[].vatrate` | object |  |
| `records[].vatrateID` | number |  |
| `records[].vatrateIDrange1` | number |  |
| `records[].vatrateIDrange2` | number |  |
| `records[].vatSumRange1` | number |  |
| `records[].vatSumRange2` | number |  |
| `records[].warehouseID` | number |  |
| `records[].warehouseName` | string |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-points-of-sale.md) for the provider-specific parameters and requirements.

