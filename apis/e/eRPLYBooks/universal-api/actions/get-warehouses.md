# ERPLY Books: Get Warehouses

Retrieves warehouse records from ERPLY Books.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-warehouses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-warehouses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-warehouses?${params}`, {
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
          "address": "string",
          "address2": "string",
          "addressID": 1,
          "assortmentID": 1,
          "bankAccountNumber": "string",
          "bankName": "Ava Chen",
          "city": "string",
          "code": "string",
          "companyCode": "string",
          "companyName": "Ava Chen",
          "companyVatNumber": "string",
          "country": "string",
          "defaultCustomerGroupID": 1,
          "email": "ava@example.com",
          "fax": "string",
          "iban": "string",
          "isOfflineInventory": 1,
          "name": "Ava Chen",
          "phone": "string",
          "pricelistID": "string",
          "pricelistID2": "string",
          "pricelistID3": "string",
          "pricelistID4": 1,
          "pricelistID5": 1,
          "state": "string",
          "stateGroup": "string",
          "storeGroups": "string",
          "storeRegionID": 1,
          "street": "string",
          "swift": "string",
          "timeZone": "string",
          "usesLocalQuickButtons": 1,
          "warehouseID": "string",
          "website": "string",
          "ZIPcode": "string"
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
| `records[].address` | string |  |
| `records[].address2` | string |  |
| `records[].addressID` | number |  |
| `records[].assortmentID` | number |  |
| `records[].bankAccountNumber` | string |  |
| `records[].bankName` | string |  |
| `records[].city` | string |  |
| `records[].code` | string |  |
| `records[].companyCode` | string |  |
| `records[].companyName` | string |  |
| `records[].companyVatNumber` | string |  |
| `records[].country` | string |  |
| `records[].defaultCustomerGroupID` | number |  |
| `records[].email` | string |  |
| `records[].fax` | string |  |
| `records[].iban` | string |  |
| `records[].isOfflineInventory` | number |  |
| `records[].name` | string |  |
| `records[].phone` | string |  |
| `records[].pricelistID` | string |  |
| `records[].pricelistID2` | string |  |
| `records[].pricelistID3` | string |  |
| `records[].pricelistID4` | number |  |
| `records[].pricelistID5` | number |  |
| `records[].state` | string |  |
| `records[].stateGroup` | string |  |
| `records[].storeGroups` | string |  |
| `records[].storeRegionID` | number |  |
| `records[].street` | string |  |
| `records[].swift` | string |  |
| `records[].timeZone` | string |  |
| `records[].usesLocalQuickButtons` | number |  |
| `records[].warehouseID` | string |  |
| `records[].website` | string |  |
| `records[].ZIPcode` | string |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-warehouses.md) for the provider-specific parameters and requirements.

