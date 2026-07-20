# Track-POD: Update Order

Updates an existing order in Track-POD.

```
PUT https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Address` | string | no | Delivery address. |
| `AddressLat` | number | no | Delivery latitude. |
| `AddressLon` | number | no | Delivery longitude. |
| `AddressZone` | string | no | Delivery address zone. |
| `Barcode` | string | no | Order barcode. |
| `Client` | string | no | Client name. |
| `COD` | number | no | Cash on delivery amount. |
| `ContactName` | string | no | Recipient contact name. |
| `CustomerReferenceId` | string | no | Customer reference identifier. |
| `CustomFields[0].Id` | string | no | First custom field identifier. |
| `CustomFields[0].Value` | string | no | First custom field value. |
| `CustomFields[1].Id` | string | no | Second custom field identifier. |
| `CustomFields[1].Value` | string | no | Second custom field value. |
| `Date` | string | no | Order date and time. |
| `Depot` | string | no | Depot name. |
| `Email` | string | no | Recipient email. |
| `GoodsList[0].Cost` | number | no | First goods cost. |
| `GoodsList[0].GoodsBarcode` | string | no | First goods barcode. |
| `GoodsList[0].GoodsId` | string | no | First goods item identifier. |
| `GoodsList[0].GoodsName` | string | no | First goods item name. |
| `GoodsList[0].GoodsUnit` | string | no | First goods unit. |
| `GoodsList[0].Note` | string | no | First goods note. |
| `GoodsList[0].OrderLineBarcode` | string | no | First goods order-line barcode. |
| `GoodsList[0].OrderLineId` | string | no | First goods line identifier. |
| `GoodsList[0].Quantity` | number | no | First goods quantity. |
| `GoodsList[1].Cost` | number | no | Second goods cost. |
| `GoodsList[1].GoodsBarcode` | string | no | Second goods barcode. |
| `GoodsList[1].GoodsId` | string | no | Second goods item identifier. |
| `GoodsList[1].GoodsName` | string | no | Second goods item name. |
| `GoodsList[1].GoodsUnit` | string | no | Second goods unit. |
| `GoodsList[1].Note` | string | no | Second goods note. |
| `GoodsList[1].OrderLineBarcode` | string | no | Second goods order-line barcode. |
| `GoodsList[1].OrderLineId` | string | no | Second goods line identifier. |
| `GoodsList[1].Quantity` | number | no | Second goods quantity. |
| `Id` | string | no | Order identifier. |
| `InvoiceId` | string | no | Invoice identifier. |
| `Note` | string | no | Order note. |
| `NotificationsPolicy.AtDepartureNotificationEnabled` | boolean | no | Send a departure notification. |
| `NotificationsPolicy.AtRouteStartNotificationEnabled` | boolean | no | Send a route-start notification. |
| `NotificationsPolicy.EnRouteNotificationEnabled` | boolean | no | Send an en-route notification. |
| `NotificationsPolicy.PriorToRouteNotificationEnabled` | boolean | no | Send a prior-to-route notification. |
| `Number` | string | no | Order number. |
| `Pallets` | number | no | Order pallets. |
| `Phone` | string | no | Recipient phone number. |
| `PickupOrder.Address` | string | no | Pickup address. |
| `PickupOrder.AddressId` | string | no | Pickup address identifier. |
| `PickupOrder.AddressLat` | number | no | Pickup latitude. |
| `PickupOrder.AddressLon` | number | no | Pickup longitude. |
| `PickupOrder.AddressZone` | string | no | Pickup address zone. |
| `PickupOrder.Client` | string | no | Pickup client name. |
| `PickupOrder.ClientId` | string | no | Pickup client identifier. |
| `PickupOrder.COD` | number | no | Pickup cash on delivery amount. |
| `PickupOrder.ContactName` | string | no | Pickup contact name. |
| `PickupOrder.CustomFields[0].Id` | string | no | First pickup custom field identifier. |
| `PickupOrder.CustomFields[0].Value` | string | no | First pickup custom field value. |
| `PickupOrder.CustomFields[1].Id` | string | no | Second pickup custom field identifier. |
| `PickupOrder.CustomFields[1].Value` | string | no | Second pickup custom field value. |
| `PickupOrder.Email` | string | no | Pickup email. |
| `PickupOrder.Note` | string | no | Pickup note. |
| `PickupOrder.Phone` | string | no | Pickup phone number. |
| `PickupOrder.ServiceTime` | number | no | Pickup service time. |
| `PickupOrder.TimeSlotFrom` | string | no | Pickup time window start. |
| `PickupOrder.TimeSlotTo` | string | no | Pickup time window end. |
| `Priority` | string | no | Order priority. One of: `0`, `1`, `2`. |
| `ServiceTime` | number | no | Planned service time. |
| `Shipper` | string | no | Shipper name. |
| `TeamCode` | string | no | Team code. |
| `TimeSlotFrom` | string | no | Start of the delivery time window. |
| `TimeSlotTo` | string | no | End of the delivery time window. |
| `Type` | number | no | Order type. |
| `updateAddressGps` | boolean | no | Force-update existing address latitude/longitude from the payload. Default: `false`. |
| `Volume` | number | no | Order volume. |
| `Weight` | number | no | Order weight. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Detail": "string",
      "Status": 1,
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Detail` | string | A human-readable explanation specific to this response. |
| `Status` | number | The HTTP status code for the response |
| `Title` | string | A short, human-readable summary of the response |

## Native endpoint

Through the native Track-POD API, this operation is `PUT /Order` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

