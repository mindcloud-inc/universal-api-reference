# Logiwa Legacy WMS: List Inventory Stock Levels

By using this endpoint, the users can obtain their current inventories based on the locations and also they may obtain some attributes such as Lot Number, and Expiration Date. The data obtained from this endpoint is raw data, the users may calculate the stock according to their logic.

```
GET https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-inventory-stock-levels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-inventory-stock-levels?connectionId=$CONNECTION_ID&warehouseID=string&depoID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "warehouseID": "string",
  "depoID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-inventory-stock-levels?${params}`, {
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
| `brand` | string | no |  |
| `itemGroup` | string | no |  |
| `location` | string | no |  |
| `lotNumber` | string | no |  |
| `warehouseID` | string | yes |  |
| `itemCode` | string | no |  |
| `depoID` | string | yes |  |
| `expirationDate` | string | no |  |
| `isDamaged` | boolean | no |  |
| `isLocked` | boolean | no |  |
| `isPickable` | boolean | no |  |
| `lastModifiedDateEnd` | string | no |  |
| `lastModifiedDateStart` | string | no |  |
| `locationZone` | string | no |  |
| `openToSales` | boolean | no |  |
| `packType` | string | no |  |
| `pickingType` | string | no |  |
| `productionDate` | string | no |  |
| `quarantineReason` | string | no |  |
| `stockReferenceNo` | string | no |  |
| `suitabilityReason` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/GetAvailableStockInfo` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inventory-stock-levels.md) for the provider-specific parameters and requirements.

