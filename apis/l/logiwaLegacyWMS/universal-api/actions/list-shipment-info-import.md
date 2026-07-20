# Logiwa Legacy WMS: List Shipment Info - Import



```
POST https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-shipment-info-import
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-shipment-info-import" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-shipment-info-import', {
  method: 'POST',
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
| `warehouseOrderID` | number | no |  |
| `warehouseOrderCode` | string | no |  |
| `inventorySiteID` | number | no |  |
| `depositorID` | number | no |  |
| `warehouseID` | number | no |  |
| `shipmentDateTimeStart` | string | no |  |
| `shipmentDateTimeEnd` | string | no |  |
| `sSCC` | string | no |  |
| `warehouseOrderTypeID` | number | no |  |
| `locationCode` | string | no |  |
| `inventoryItemID` | number | no |  |
| `lotBatchNo` | string | no |  |
| `carrierID` | number | no |  |
| `channelOrderCode` | string | no |  |
| `carrierTrackingNumber` | string | no |  |
| `orderDateStart` | string | no |  |
| `orderDateEnd` | string | no |  |
| `channelID` | number | no |  |
| `storeName` | string | no |  |
| `country` | string | no |  |
| `state` | string | no |  |
| `city` | string | no |  |
| `carrierAddressType` | string | no |  |
| `itemCode` | string | no |  |
| `itemDescription` | string | no |  |
| `snapshotDatetimeStart` | string | no |  |
| `snapshotDatetimeEnd` | string | no |  |
| `isExported` | boolean | no |  |
| `pageSize` | number | no |  |
| `selectedPageIndex` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/ShipmentReportAllSearch` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipment-info-import.md) for the provider-specific parameters and requirements.

