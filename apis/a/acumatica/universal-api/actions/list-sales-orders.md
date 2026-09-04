# Acumatica: List Sales Orders



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-sales-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-sales-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-sales-orders?${params}`, {
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
| `select` | string | no |  |
| `expand` | string | no |  |
| `filter` | string | no |  |

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
| `Description.value` | string |  |
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

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/SalesOrder` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-orders.md) for the provider-specific parameters and requirements.

