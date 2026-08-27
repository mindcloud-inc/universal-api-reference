# Acumatica: Create/Update Shipment



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-update-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-update-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-update-shipment', {
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
| `CustomerID.value` | string | no |  |
| `Description.value` | string | no |  |
| `Details[].Allocations[].InventoryID.value` | string | no |  |
| `Details[].Allocations[].LocationID` | object | no |  |
| `Details[].Allocations[].LocationID.value` | string | no |  |
| `Details[].Allocations[].LotSerialNbr.value` | string | no |  |
| `Details[].Allocations[].Qty.value` | number | no |  |
| `Details[].Allocations[].UsrLPNbr.value` | string | no |  |
| `Details[].LocationID.value` | string | no |  |
| `Details[].LotSerialNbr.value` | string | no |  |
| `Details[].OrderLineNbr` | object | no |  |
| `Details[].OrderLineNbr.value` | number | no |  |
| `Details[].OrderNbr.value` | string | no |  |
| `Details[].OrderType.value` | string | no |  |
| `Details[].ShippedQty.value` | number | no |  |
| `Details[].UsrLPNbr.value` | string | no |  |
| `expand` | string | no |  |
| `FreightCost.value` | string | no |  |
| `FreightPrice.value` | string | no |  |
| `Hold.value` | boolean | no |  |
| `LocationID.value` | string | no |  |
| `Note.value` | string | no |  |
| `Operation.value` | string | no |  |
| `Packages[].BoxID` | object | no |  |
| `Packages[].BoxID.value` | string | no |  |
| `Packages[].Description.value` | string | no |  |
| `Packages[].Height.value` | number | no |  |
| `Packages[].Length.value` | number | no |  |
| `Packages[].TrackingNbr.value` | string | no |  |
| `Packages[].Type.value` | string | no |  |
| `Packages[].Weight.value` | number | no |  |
| `Packages[].Width.value` | number | no |  |
| `ResidentialDelivery.value` | boolean | no |  |
| `ShipmentDate.value` | string | no |  |
| `ShippedVolume.value` | number | no |  |
| `ShippedWeight.value` | number | no |  |
| `ShippingSettings.AddressLine1.value` | string | no |  |
| `ShippingSettings.AddressLine2.value` | string | no |  |
| `ShippingSettings.Attention.value` | string | no |  |
| `ShippingSettings.BusinessName.value` | string | no |  |
| `ShippingSettings.City.value` | string | no |  |
| `ShippingSettings.Country.value` | string | no |  |
| `ShippingSettings.Email.value` | string | no |  |
| `ShippingSettings.Phone1.value` | string | no |  |
| `ShippingSettings.PostalCode.value` | string | no |  |
| `ShippingSettings.ShipToAddressOverride.value` | boolean | no |  |
| `ShippingSettings.ShipToContactOverride` | object | no |  |
| `ShippingSettings.ShipToContactOverride.value` | boolean | no |  |
| `ShippingSettings.State.value` | string | no |  |
| `ShipVia.value` | string | no |  |
| `Type.value` | string | no |  |
| `UsrCarrier.value` | string | no |  |
| `UsrDriverName.value` | string | no |  |
| `UsrLogiwaConf.value` | boolean | no |  |
| `UsrServiceLevel.value` | string | no |  |
| `UsrServiceLvl.value` | string | no |  |
| `UsrStop.value` | number | no |  |
| `WarehouseID.value` | string | no |  |
| `Details[].Allocations[].LotSerialNbr` | object | no |  |
| `Details[].ShippedQty` | object | no |  |
| `Packages[].Description` | object | no |  |
| `ShippingSettings.BusinessName` | object | no |  |
| `Type` | object | no |  |
| `Details[].Allocations[].Qty` | object | no |  |
| `Details[].OrderNbr` | object | no |  |
| `Hold` | object | no |  |
| `Packages[].TrackingNbr` | object | no |  |
| `ShippingSettings.Attention` | object | no |  |
| `Details[].Allocations[].UsrLPNbr` | object | no |  |
| `Details[].OrderType` | object | no |  |
| `Operation` | object | no |  |
| `Packages[].Type` | object | no |  |
| `ShippingSettings.Phone1` | object | no |  |
| `CustomerID` | object | no |  |
| `Details[].Allocations[].InventoryID` | object | no |  |
| `Details[].LotSerialNbr` | object | no |  |
| `Packages[].Weight` | object | no |  |
| `ShippingSettings.Email` | object | no |  |
| `Details[].LocationID` | object | no |  |
| `LocationID` | object | no |  |
| `Packages[].Length` | object | no |  |
| `ShippingSettings.ShipToAddressOverride` | object | no |  |
| `Details[].UsrLPNbr` | object | no |  |
| `Packages[].Width` | object | no |  |
| `ShipmentDate` | object | no |  |
| `ShippingSettings.AddressLine1` | object | no |  |
| `Details[].Allocations[]` | array | no |  |
| `Packages[].Height` | object | no |  |
| `ShippingSettings.AddressLine2` | object | no |  |
| `WarehouseID` | object | no |  |
| `ShippingSettings.City` | object | no |  |
| `UsrDriverName` | object | no |  |
| `ShippingSettings.State` | object | no |  |
| `UsrStop` | object | no |  |
| `ShippingSettings.PostalCode` | object | no |  |
| `UsrLogiwaConf` | object | no |  |
| `Description` | object | no |  |
| `ShippingSettings.Country` | object | no |  |
| `FreightCost` | object | no |  |
| `FreightPrice` | object | no |  |
| `ResidentialDelivery` | object | no |  |
| `ShipVia` | object | no |  |
| `ShippedWeight` | object | no |  |
| `ShippedVolume` | object | no |  |
| `Note` | object | no |  |
| `UsrCarrier` | object | no |  |
| `UsrServiceLevel` | object | no |  |
| `ShippingSettings` | object | no |  |
| `Details[]` | array | no |  |
| `Packages[]` | array | no |  |
| `UsrServiceLvl` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumatica API returns.

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Shipment` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-update-shipment.md) for the provider-specific parameters and requirements.

