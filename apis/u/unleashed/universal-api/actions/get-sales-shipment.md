# Unleashed: Get Sales Shipment

Retrieves a sales shipment from your Unleashed account.

```
GET https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/get-sales-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/get-sales-shipment?connectionId=$CONNECTION_ID&salesShipmentGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "salesShipmentGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/get-sales-shipment?${params}`, {
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
| `salesShipmentGuid` | string | yes | The Unleashed sales shipment GUID. |

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

Through the native Unleashed API, this operation is `GET /SalesShipments/:salesShipmentGuid` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-shipment.md) for the provider-specific parameters and requirements.

