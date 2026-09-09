# Acumatica: List Shipments



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-shipments?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `ShipmentNbr,Status,CustomerID`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `Details,Packages`. |
| `filter` | string | no | Acumatica OData filter expression used to qualify returned records. Example: `Status eq 'Open'`. |
| `custom` | string | no | Comma-separated custom fields to return. Example: `ShipmentNbr,Status`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "files:put": "https://example.com",
        "self": "https://example.com"
      },
      "BaseCurrencyID": {
        "value": "string"
      },
      "ControlQty": {
        "value": 1
      },
      "CreatedDateTime": {
        "value": "string"
      },
      "CurrencyRate": {
        "value": 1
      },
      "CurrencyViewState": {
        "value": true
      },
      "CustomerID": {
        "value": "string"
      },
      "EffectiveDate": {
        "value": "string"
      },
      "FreightAmount": {
        "value": 1
      },
      "FreightCost": {
        "value": 1
      },
      "FreightCurrencyID": {
        "value": "string"
      },
      "GroundCollect": {
        "value": true
      },
      "Hold": {
        "value": true
      },
      "id": "string",
      "Insurance": {
        "value": true
      },
      "LastModifiedDateTime": {
        "value": "string"
      },
      "LocationID": {
        "value": "string"
      },
      "note": {
        "value": "string"
      },
      "Operation": {
        "value": "string"
      },
      "OverrideFreightPrice": {
        "value": true
      },
      "Owner": {
        "value": "string"
      },
      "PackageCount": {
        "value": 1
      },
      "PackageWeight": {
        "value": 1
      },
      "Picked": {
        "value": true
      },
      "ReciprocalRate": {
        "value": 1
      },
      "ResidentialDelivery": {
        "value": true
      },
      "rowNumber": 1,
      "SaturdayDelivery": {
        "value": true
      },
      "ShipmentDate": {
        "value": "string"
      },
      "ShipmentNbr": {
        "value": "string"
      },
      "ShippedQty": {
        "value": 1
      },
      "ShippedVolume": {
        "value": 1
      },
      "ShippedWeight": {
        "value": 1
      },
      "Status": {
        "value": "string"
      },
      "Type": {
        "value": "string"
      },
      "UseCustomersAccount": {
        "value": true
      },
      "WarehouseID": {
        "value": "string"
      },
      "WorkgroupID": {
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.files:put` | string |  |
| `_links.self` | string |  |
| `BaseCurrencyID.value` | string |  |
| `ControlQty.value` | number |  |
| `CreatedDateTime.value` | string |  |
| `CurrencyRate.value` | number |  |
| `CurrencyViewState.value` | boolean |  |
| `CustomerID.value` | string |  |
| `EffectiveDate.value` | string |  |
| `FreightAmount.value` | number |  |
| `FreightCost.value` | number |  |
| `FreightCurrencyID.value` | string |  |
| `GroundCollect.value` | boolean |  |
| `Hold.value` | boolean |  |
| `id` | string |  |
| `Insurance.value` | boolean |  |
| `LastModifiedDateTime.value` | string |  |
| `LocationID.value` | string |  |
| `note.value` | string |  |
| `Operation.value` | string |  |
| `OverrideFreightPrice.value` | boolean |  |
| `Owner.value` | string |  |
| `PackageCount.value` | number |  |
| `PackageWeight.value` | number |  |
| `Picked.value` | boolean |  |
| `ReciprocalRate.value` | number |  |
| `ResidentialDelivery.value` | boolean |  |
| `rowNumber` | number |  |
| `SaturdayDelivery.value` | boolean |  |
| `ShipmentDate.value` | string |  |
| `ShipmentNbr.value` | string |  |
| `ShippedQty.value` | number |  |
| `ShippedVolume.value` | number |  |
| `ShippedWeight.value` | number |  |
| `Status.value` | string |  |
| `Type.value` | string |  |
| `UseCustomersAccount.value` | boolean |  |
| `WarehouseID.value` | string |  |
| `WorkgroupID.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Shipment` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-shipments.md) for the provider-specific parameters and requirements.

