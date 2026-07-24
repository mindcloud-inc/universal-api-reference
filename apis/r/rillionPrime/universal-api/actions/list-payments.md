# Rillion Prime Pay: List Payments



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payments?${params}`, {
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
| `searchTerm` | string | no | Filter results by search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "company": "string",
      "companyName": "Ava Chen",
      "currency": "string",
      "currentPaymentProviderStage": "string",
      "currentPaymentProviderStatus": "string",
      "details": {
        "checkImageUrl": {},
        "clearingDate": "string",
        "foreignAmountMinorUnits": {},
        "fxCurrency": {},
        "fxRate": {},
        "instrumentNumber": "string",
        "issuedDate": "string",
        "reconciliationId": "string",
        "trackingId": "string",
        "usdAmount": {}
      },
      "discountAmount": 1,
      "discountApplied": true,
      "discountDate": {},
      "dueDate": "string",
      "events": [
        {
          "amountCents": 1,
          "category": "string",
          "description": "string",
          "eventCode": "string",
          "eventName": "Ava Chen",
          "method": "string",
          "stage": "string",
          "status": "string",
          "timestamp": "string"
        }
      ],
      "externalId": {},
      "externalSource": {},
      "fxRate": {},
      "fxRateRetrievedAt": {},
      "fxRateType": "string",
      "id": "string",
      "invoiceDate": "string",
      "invoiceNumber": "string",
      "lastInvoiceApprovalDate": "string",
      "lastInvoiceApproverNames": "Ava Chen",
      "paymentDate": "string",
      "paymentMethod": "string",
      "paymentReferenceId": "string",
      "paymentSentByName": "Ava Chen",
      "paymentSentOnDate": "string",
      "paymentStatus": "string",
      "paymentStatusLastChangeDate": "string",
      "processingDates": {
        "fundingReceivedByProviderDate": "string",
        "paymentSettledDate": "string",
        "sentFromProviderDate": "string",
        "sentToProviderDate": "string"
      },
      "scheduleDate": "string",
      "supplier": "string",
      "supplierInvoiceNo": "string",
      "supplierName": "Ava Chen",
      "supplierStatus": "string",
      "usdAmount": 1,
      "voucherNo": "string",
      "voucherSeries": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `company` | string |  |
| `companyName` | string |  |
| `currency` | string |  |
| `currentPaymentProviderStage` | string |  |
| `currentPaymentProviderStatus` | string |  |
| `details.checkImageUrl` | object |  |
| `details.clearingDate` | string |  |
| `details.foreignAmountMinorUnits` | object |  |
| `details.fxCurrency` | object |  |
| `details.fxRate` | object |  |
| `details.instrumentNumber` | string |  |
| `details.issuedDate` | string |  |
| `details.reconciliationId` | string |  |
| `details.trackingId` | string |  |
| `details.usdAmount` | object |  |
| `discountAmount` | number |  |
| `discountApplied` | boolean |  |
| `discountDate` | object |  |
| `dueDate` | string |  |
| `events[].amountCents` | number |  |
| `events[].category` | string |  |
| `events[].description` | string |  |
| `events[].eventCode` | string |  |
| `events[].eventName` | string |  |
| `events[].method` | string |  |
| `events[].stage` | string |  |
| `events[].status` | string |  |
| `events[].timestamp` | string |  |
| `externalId` | object |  |
| `externalSource` | object |  |
| `fxRate` | object |  |
| `fxRateRetrievedAt` | object |  |
| `fxRateType` | string |  |
| `id` | string |  |
| `invoiceDate` | string |  |
| `invoiceNumber` | string |  |
| `lastInvoiceApprovalDate` | string |  |
| `lastInvoiceApproverNames` | string |  |
| `paymentDate` | string |  |
| `paymentMethod` | string |  |
| `paymentReferenceId` | string |  |
| `paymentSentByName` | string |  |
| `paymentSentOnDate` | string |  |
| `paymentStatus` | string |  |
| `paymentStatusLastChangeDate` | string |  |
| `processingDates.fundingReceivedByProviderDate` | string |  |
| `processingDates.paymentSettledDate` | string |  |
| `processingDates.sentFromProviderDate` | string |  |
| `processingDates.sentToProviderDate` | string |  |
| `scheduleDate` | string |  |
| `supplier` | string |  |
| `supplierInvoiceNo` | string |  |
| `supplierName` | string |  |
| `supplierStatus` | string |  |
| `usdAmount` | number |  |
| `voucherNo` | string |  |
| `voucherSeries` | string |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `GET /payment` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

