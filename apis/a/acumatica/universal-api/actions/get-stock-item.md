# Acumatica: Get Stock Item



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-stock-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-stock-item?connectionId=$CONNECTION_ID&id=2a113b2c-d87f-e411-beca-00b56d0561c2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2a113b2c-d87f-e411-beca-00b56d0561c2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-stock-item?${params}`, {
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
| `id` | string | yes | The Acumatica entity ID (GUID) returned in the record's id field. Example: `2a113b2c-d87f-e411-beca-00b56d0561c2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `InventoryID,Description,ItemStatus`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `WarehouseDetails`. |
| `custom` | string | no | Comma-separated custom fields to return. Example: `InventoryID,Description`. |

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
      "AverageCost": {
        "value": 1
      },
      "BaseUOM": {
        "value": "string"
      },
      "COGSAccount": {
        "value": "string"
      },
      "COGSSubaccount": {
        "value": "string"
      },
      "Content": {
        "value": "string"
      },
      "CurrentStdCost": {
        "value": 1
      },
      "DefaultIssueLocationID": {
        "value": "string"
      },
      "DefaultPrice": {
        "value": 1
      },
      "DefaultReceiptLocationID": {
        "value": "string"
      },
      "DefaultWarehouseID": {
        "value": "string"
      },
      "Description": {
        "value": "string"
      },
      "DimensionVolume": {
        "value": 1
      },
      "DimensionWeight": {
        "value": 1
      },
      "id": "string",
      "ImageUrl": {
        "value": "https://example.com"
      },
      "InventoryAccount": {
        "value": "string"
      },
      "InventoryID": {
        "value": "string"
      },
      "InventorySubaccount": {
        "value": "string"
      },
      "IsAKit": {
        "value": true
      },
      "ItemClass": {
        "value": "string"
      },
      "ItemStatus": {
        "value": "string"
      },
      "ItemType": {
        "value": "string"
      },
      "LandedCostVarianceAccount": {
        "value": "string"
      },
      "LandedCostVarianceSubaccount": {
        "value": "string"
      },
      "LastCost": {
        "value": 1
      },
      "LastModified": {
        "value": "string"
      },
      "LastStdCost": {
        "value": 1
      },
      "LotSerialClass": {
        "value": "string"
      },
      "Markup": {
        "value": 1
      },
      "MaxCost": {
        "value": 1
      },
      "MinCost": {
        "value": 1
      },
      "MinMarkup": {
        "value": 1
      },
      "MSRP": {
        "value": 1
      },
      "note": {
        "value": "string"
      },
      "PackagingOption": {
        "value": "string"
      },
      "PackSeparately": {
        "value": true
      },
      "PendingStdCost": {
        "value": 1
      },
      "POAccrualAccount": {
        "value": "string"
      },
      "POAccrualSubaccount": {
        "value": "string"
      },
      "PostingClass": {
        "value": "string"
      },
      "PurchasePriceVarianceAccount": {
        "value": "string"
      },
      "PurchasePriceVarianceSubaccount": {
        "value": "string"
      },
      "PurchaseUOM": {
        "value": "string"
      },
      "ReasonCodeSubaccount": {
        "value": "string"
      },
      "rowNumber": 1,
      "SalesAccount": {
        "value": "string"
      },
      "SalesSubaccount": {
        "value": "string"
      },
      "SalesUOM": {
        "value": "string"
      },
      "StandardCostRevaluationAccount": {
        "value": "string"
      },
      "StandardCostRevaluationSubaccount": {
        "value": "string"
      },
      "StandardCostVarianceAccount": {
        "value": "string"
      },
      "StandardCostVarianceSubaccount": {
        "value": "string"
      },
      "SubjectToCommission": {
        "value": true
      },
      "TaxCategory": {
        "value": "string"
      },
      "ValuationMethod": {
        "value": "string"
      },
      "VolumeUOM": {
        "value": "string"
      },
      "WeightUOM": {
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
| `AverageCost.value` | number |  |
| `BaseUOM.value` | string |  |
| `COGSAccount.value` | string |  |
| `COGSSubaccount.value` | string |  |
| `Content.value` | string |  |
| `CurrentStdCost.value` | number |  |
| `DefaultIssueLocationID.value` | string |  |
| `DefaultPrice.value` | number |  |
| `DefaultReceiptLocationID.value` | string |  |
| `DefaultWarehouseID.value` | string |  |
| `Description.value` | string |  |
| `DimensionVolume.value` | number |  |
| `DimensionWeight.value` | number |  |
| `id` | string |  |
| `ImageUrl.value` | string |  |
| `InventoryAccount.value` | string |  |
| `InventoryID.value` | string |  |
| `InventorySubaccount.value` | string |  |
| `IsAKit.value` | boolean |  |
| `ItemClass.value` | string |  |
| `ItemStatus.value` | string |  |
| `ItemType.value` | string |  |
| `LandedCostVarianceAccount.value` | string |  |
| `LandedCostVarianceSubaccount.value` | string |  |
| `LastCost.value` | number |  |
| `LastModified.value` | string |  |
| `LastStdCost.value` | number |  |
| `LotSerialClass.value` | string |  |
| `Markup.value` | number |  |
| `MaxCost.value` | number |  |
| `MinCost.value` | number |  |
| `MinMarkup.value` | number |  |
| `MSRP.value` | number |  |
| `note.value` | string |  |
| `PackagingOption.value` | string |  |
| `PackSeparately.value` | boolean |  |
| `PendingStdCost.value` | number |  |
| `POAccrualAccount.value` | string |  |
| `POAccrualSubaccount.value` | string |  |
| `PostingClass.value` | string |  |
| `PurchasePriceVarianceAccount.value` | string |  |
| `PurchasePriceVarianceSubaccount.value` | string |  |
| `PurchaseUOM.value` | string |  |
| `ReasonCodeSubaccount.value` | string |  |
| `rowNumber` | number |  |
| `SalesAccount.value` | string |  |
| `SalesSubaccount.value` | string |  |
| `SalesUOM.value` | string |  |
| `StandardCostRevaluationAccount.value` | string |  |
| `StandardCostRevaluationSubaccount.value` | string |  |
| `StandardCostVarianceAccount.value` | string |  |
| `StandardCostVarianceSubaccount.value` | string |  |
| `SubjectToCommission.value` | boolean |  |
| `TaxCategory.value` | string |  |
| `ValuationMethod.value` | string |  |
| `VolumeUOM.value` | string |  |
| `WeightUOM.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/StockItem/:id` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stock-item.md) for the provider-specific parameters and requirements.

