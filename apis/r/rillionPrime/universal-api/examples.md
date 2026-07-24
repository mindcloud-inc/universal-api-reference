# Rillion Prime Pay Universal API Examples

These examples use the MindCloud API key and Rillion Prime Pay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Payments



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

Example response:

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

See the full [List Payments action reference](actions/list-payments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rillionPrime/latest/actions/list-payments).

## Approve Payments



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/approve-payments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/approve-payments', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "failed": {
        "duplicateStatus": 1
      },
      "successfull": 1
    }
  ],
  "meta": {}
}
```

See the full [Approve Payments action reference](actions/approve-payments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rillionPrime/latest/actions/approve-payments).
