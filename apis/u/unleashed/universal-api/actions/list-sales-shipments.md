# Unleashed: List Sales Shipments

Retrieves sales shipments from your Unleashed account.

```
GET https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-sales-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-sales-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-sales-shipments?${params}`, {
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
      "comments": "string",
      "createdOn": "string",
      "customer": {},
      "dispatchDate": "string",
      "guid": "string",
      "lastModifiedOn": "string",
      "orderGuid": "string",
      "orderNumber": "string",
      "salesShipmentLines": [
        {}
      ],
      "shipmentNumber": "string",
      "shipmentStatus": "string",
      "shipmentStatusEnum": 1,
      "shippingCompany": "string",
      "totalCommercialValue": 1,
      "trackingNumber": "string",
      "warehouse": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `createdOn` | string |  |
| `customer` | object |  |
| `dispatchDate` | string |  |
| `guid` | string |  |
| `lastModifiedOn` | string |  |
| `orderGuid` | string |  |
| `orderNumber` | string |  |
| `salesShipmentLines` | array<object> |  |
| `shipmentNumber` | string |  |
| `shipmentStatus` | string |  |
| `shipmentStatusEnum` | number |  |
| `shippingCompany` | string |  |
| `totalCommercialValue` | number |  |
| `trackingNumber` | string |  |
| `warehouse` | object |  |

## Native endpoint

Through the native Unleashed API, this operation is `GET /SalesShipments/:pageNumber` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-shipments.md) for the provider-specific parameters and requirements.

