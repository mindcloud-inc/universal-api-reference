# Cin7 Core: List Sales



```
GET https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/list-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cin7 Core `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/list-sales?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/list-sales?${params}`, {
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
| `Search` | string | no |  |
| `CreatedSince` | string | no |  |
| `UpdatedSince` | string | no |  |
| `OrderStatus` | string | no |  |
| `ExternalID` | string | no |  |
| `Status` | string | no |  |
| `orderLocationID` | string | no |  |
| `combinedPickStatus` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseCurrency": "string",
      "combinedInvoiceStatus": "string",
      "combinedPackingStatus": "string",
      "combinedPaymentStatus": "string",
      "combinedPaymentTotal": 1,
      "combinedPickingStatus": "string",
      "combinedShippingStatus": "string",
      "combinedTrackingNumbers": "string",
      "creditNoteNumber": {},
      "creditNoteStatus": "string",
      "customer": "string",
      "customerCurrency": "string",
      "customerID": "string",
      "customerReference": "string",
      "externalID": "string",
      "fulFilmentStatus": "string",
      "invoiceAmount": 1,
      "invoiceDate": "string",
      "invoiceDueDate": "string",
      "invoiceNumber": "string",
      "orderDate": "string",
      "orderLocationID": "string",
      "orderNumber": "string",
      "orderStatus": "string",
      "paidAmount": 1,
      "quoteStatus": "string",
      "restockStatus": "string",
      "saleID": "string",
      "saleInvoicesTotalAmount": 1,
      "shipBy": "string",
      "sourceChannel": "string",
      "status": "string",
      "type": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseCurrency` | string |  |
| `combinedInvoiceStatus` | string |  |
| `combinedPackingStatus` | string |  |
| `combinedPaymentStatus` | string |  |
| `combinedPaymentTotal` | number |  |
| `combinedPickingStatus` | string |  |
| `combinedShippingStatus` | string |  |
| `combinedTrackingNumbers` | string |  |
| `creditNoteNumber` | object |  |
| `creditNoteStatus` | string |  |
| `customer` | string |  |
| `customerCurrency` | string |  |
| `customerID` | string |  |
| `customerReference` | string |  |
| `externalID` | string |  |
| `fulFilmentStatus` | string |  |
| `invoiceAmount` | number |  |
| `invoiceDate` | string |  |
| `invoiceDueDate` | string |  |
| `invoiceNumber` | string |  |
| `orderDate` | string |  |
| `orderLocationID` | string |  |
| `orderNumber` | string |  |
| `orderStatus` | string |  |
| `paidAmount` | number |  |
| `quoteStatus` | string |  |
| `restockStatus` | string |  |
| `saleID` | string |  |
| `saleInvoicesTotalAmount` | number |  |
| `shipBy` | string |  |
| `sourceChannel` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Cin7 Core API, this operation is `GET saleList` (base URL `https://inventory.dearsystems.com/externalapi/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales.md) for the provider-specific parameters and requirements.

