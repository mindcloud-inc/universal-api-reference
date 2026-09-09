# Acumatica: Create or Update Sales Order



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "OrderType.value": "SO",
  "CustomerID.value": "AACUSTOMER",
  "Details[]": [
    {}
  ],
  "Details[].InventoryID.value": "string",
  "Details[].OrderQty.value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/create-or-update-sales-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "OrderType.value": "SO",
    "CustomerID.value": "AACUSTOMER",
    "Details[]": [{}],
    "Details[].InventoryID.value": "string",
    "Details[].OrderQty.value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `OrderType` | object | no |  |
| `OrderType.value` | string | yes | Example: `SO`. |
| `CustomerID` | object | no |  |
| `CustomerID.value` | string | yes | Example: `AACUSTOMER`. |
| `Description` | object | no |  |
| `Description.value` | string | no | Example: `MindCloud sandbox test order`. |
| `Hold` | object | no |  |
| `Hold.value` | boolean | no | Default: `true`. |
| `Details[]` | array<object> | yes |  |
| `Details[].InventoryID` | object | no |  |
| `Details[].InventoryID.value` | string | yes |  |
| `Details[].OrderQty` | object | no |  |
| `Details[].OrderQty.value` | number | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Existing Acumatica entity GUID when updating; leave blank to create. Example: `00000000-0000-0000-0000-000000000000`. |
| `OrderNbr` | object | no |  |
| `OrderNbr.value` | string | no |  |
| `Date` | object | no |  |
| `Date.value` | date | no |  |
| `Details[].UOM` | object | no |  |
| `Details[].UOM.value` | string | no |  |
| `Details[].WarehouseID` | object | no |  |
| `Details[].WarehouseID.value` | string | no |  |

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
      "CurrencyRateTypeID": {
        "value": "string"
      },
      "CustomerID": {
        "value": "string"
      },
      "Date": {
        "value": "2026-05-07T12:00:00.000Z"
      },
      "Description": {
        "value": "string"
      },
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
      "IsTaxValid": {
        "value": true
      },
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
| `CurrencyRateTypeID.value` | string |  |
| `CustomerID.value` | string |  |
| `Date.value` | date |  |
| `Description.value` | string |  |
| `DisableAutomaticDiscountUpdate.value` | boolean |  |
| `EffectiveDate.value` | date |  |
| `Hold.value` | boolean |  |
| `id` | string |  |
| `IsTaxValid.value` | boolean |  |
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

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-sales-order.md) for the provider-specific parameters and requirements.

