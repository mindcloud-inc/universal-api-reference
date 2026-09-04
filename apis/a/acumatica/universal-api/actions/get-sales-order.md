# Acumatica: Get Sales Order



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-sales-order?connectionId=$CONNECTION_ID&orderType=SO&orderNbr=000123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderType": "SO",
  "orderNbr": "000123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-sales-order?${params}`, {
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
| `orderType` | string | yes | The Acumatica sales order type returned by List Sales Orders. Example: `SO`. |
| `orderNbr` | string | yes | The Acumatica sales order number returned by List Sales Orders. Example: `000123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Fields to return, using Acumatica $select syntax. |
| `expand` | string | no |  |
| `custom` | string | no | Custom fields to return, using Acumatica $custom syntax. |

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
      "Approved": {
        "value": true
      },
      "BaseCurrencyID": {
        "value": "string"
      },
      "BillToAddressOverride": {
        "value": true
      },
      "BillToContactOverride": {
        "value": true
      },
      "CashAccount": {
        "value": "string"
      },
      "ContactID": {
        "value": "string"
      },
      "ControlTotal": {
        "value": 1
      },
      "CreditHold": {
        "value": true
      },
      "CurrencyID": {
        "value": "string"
      },
      "CurrencyRate": {
        "value": 1
      },
      "CustomerID": {
        "value": "string"
      },
      "CustomerOrder": {
        "value": "string"
      },
      "Date": {
        "value": "2026-05-07T12:00:00.000Z"
      },
      "Details": [
        {
          "_links": {
            "files:put": "https://example.com"
          },
          "Account": {
            "value": "string"
          },
          "Amount": {
            "value": 1
          },
          "AutoCreateIssue": {
            "value": true
          },
          "AverageCost": {
            "value": 1
          },
          "Branch": {
            "value": "string"
          },
          "Commissionable": {
            "value": true
          },
          "Completed": {
            "value": true
          },
          "DiscountAmount": {
            "value": 1
          },
          "DiscountedUnitPrice": {
            "value": 1
          },
          "DiscountPercent": {
            "value": 1
          },
          "ExtendedPrice": {
            "value": 1
          },
          "FreeItem": {
            "value": true
          },
          "id": "string",
          "InventoryID": {
            "value": "string"
          },
          "LastModifiedDate": {
            "value": "2026-05-07T12:00:00.000Z"
          },
          "LineDescription": {
            "value": "string"
          },
          "LineNbr": {
            "value": 1
          },
          "LineType": {
            "value": "string"
          },
          "ManualDiscount": {
            "value": true
          },
          "MarkForPO": {
            "value": true
          },
          "note": {
            "value": "string"
          },
          "OpenQty": {
            "value": 1
          },
          "Operation": {
            "value": "string"
          },
          "OrderQty": {
            "value": 1
          },
          "OvershipThreshold": {
            "value": 1
          },
          "QtyOnShipments": {
            "value": 1
          },
          "RequestedOn": {
            "value": "2026-05-07T12:00:00.000Z"
          },
          "rowNumber": 1,
          "SalespersonID": {
            "value": "string"
          },
          "SchedOrderDate": {
            "value": "2026-05-07T12:00:00.000Z"
          },
          "ShipOn": {
            "value": "2026-05-07T12:00:00.000Z"
          },
          "ShippingRule": {
            "value": "string"
          },
          "ShipToLocation": {
            "value": "string"
          },
          "TaxCategory": {
            "value": "string"
          },
          "UnbilledAmount": {
            "value": 1
          },
          "UndershipThreshold": {
            "value": 1
          },
          "UnitCost": {
            "value": 1
          },
          "UnitPrice": {
            "value": 1
          },
          "UOM": {
            "value": "string"
          },
          "WarehouseID": {
            "value": "string"
          }
        }
      ],
      "DisableAutomaticDiscountUpdate": {
        "value": true
      },
      "EffectiveDate": {
        "value": "2026-05-07T12:00:00.000Z"
      },
      "Hold": {
        "value": true
      },
      "id": "string",
      "LastModified": {
        "value": "2026-05-07T12:00:00.000Z"
      },
      "LocationID": {
        "value": "string"
      },
      "note": {
        "value": "string"
      },
      "OrderedQty": {
        "value": 1
      },
      "OrderNbr": {
        "value": "string"
      },
      "OrderTotal": {
        "value": 1
      },
      "OrderType": {
        "value": "string"
      },
      "PaymentMethod": {
        "value": "string"
      },
      "Project": {
        "value": "string"
      },
      "ReciprocalRate": {
        "value": 1
      },
      "RequestedOn": {
        "value": "2026-05-07T12:00:00.000Z"
      },
      "rowNumber": 1,
      "ShipToAddressOverride": {
        "value": true
      },
      "ShipToContactOverride": {
        "value": true
      },
      "Status": {
        "value": "string"
      },
      "TaxTotal": {
        "value": 1
      },
      "VATExemptTotal": {
        "value": 1
      },
      "VATTaxableTotal": {
        "value": 1
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
| `Approved.value` | boolean |  |
| `BaseCurrencyID.value` | string |  |
| `BillToAddressOverride.value` | boolean |  |
| `BillToContactOverride.value` | boolean |  |
| `CashAccount.value` | string |  |
| `ContactID.value` | string |  |
| `ControlTotal.value` | number |  |
| `CreditHold.value` | boolean |  |
| `CurrencyID.value` | string |  |
| `CurrencyRate.value` | number |  |
| `CustomerID.value` | string |  |
| `CustomerOrder.value` | string |  |
| `Date.value` | date |  |
| `Details[]._links.files:put` | string |  |
| `Details[].Account.value` | string |  |
| `Details[].Amount.value` | number |  |
| `Details[].AutoCreateIssue.value` | boolean |  |
| `Details[].AverageCost.value` | number |  |
| `Details[].Branch.value` | string |  |
| `Details[].Commissionable.value` | boolean |  |
| `Details[].Completed.value` | boolean |  |
| `Details[].DiscountAmount.value` | number |  |
| `Details[].DiscountedUnitPrice.value` | number |  |
| `Details[].DiscountPercent.value` | number |  |
| `Details[].ExtendedPrice.value` | number |  |
| `Details[].FreeItem.value` | boolean |  |
| `Details[].id` | string |  |
| `Details[].InventoryID.value` | string |  |
| `Details[].LastModifiedDate.value` | date |  |
| `Details[].LineDescription.value` | string |  |
| `Details[].LineNbr.value` | number |  |
| `Details[].LineType.value` | string |  |
| `Details[].ManualDiscount.value` | boolean |  |
| `Details[].MarkForPO.value` | boolean |  |
| `Details[].note.value` | string |  |
| `Details[].OpenQty.value` | number |  |
| `Details[].Operation.value` | string |  |
| `Details[].OrderQty.value` | number |  |
| `Details[].OvershipThreshold.value` | number |  |
| `Details[].QtyOnShipments.value` | number |  |
| `Details[].RequestedOn.value` | date |  |
| `Details[].rowNumber` | number |  |
| `Details[].SalespersonID.value` | string |  |
| `Details[].SchedOrderDate.value` | date |  |
| `Details[].ShipOn.value` | date |  |
| `Details[].ShippingRule.value` | string |  |
| `Details[].ShipToLocation.value` | string |  |
| `Details[].TaxCategory.value` | string |  |
| `Details[].UnbilledAmount.value` | number |  |
| `Details[].UndershipThreshold.value` | number |  |
| `Details[].UnitCost.value` | number |  |
| `Details[].UnitPrice.value` | number |  |
| `Details[].UOM.value` | string |  |
| `Details[].WarehouseID.value` | string |  |
| `DisableAutomaticDiscountUpdate.value` | boolean |  |
| `EffectiveDate.value` | date |  |
| `Hold.value` | boolean |  |
| `id` | string |  |
| `LastModified.value` | date |  |
| `LocationID.value` | string |  |
| `note.value` | string |  |
| `OrderedQty.value` | number |  |
| `OrderNbr.value` | string |  |
| `OrderTotal.value` | number |  |
| `OrderType.value` | string |  |
| `PaymentMethod.value` | string |  |
| `Project.value` | string |  |
| `ReciprocalRate.value` | number |  |
| `RequestedOn.value` | date |  |
| `rowNumber` | number |  |
| `ShipToAddressOverride.value` | boolean |  |
| `ShipToContactOverride.value` | boolean |  |
| `Status.value` | string |  |
| `TaxTotal.value` | number |  |
| `VATExemptTotal.value` | number |  |
| `VATTaxableTotal.value` | number |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder/:orderType/:orderNbr` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-order.md) for the provider-specific parameters and requirements.

