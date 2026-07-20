# finaX Universal API Examples

These examples use the MindCloud API key and finaX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## CII Or UBL To JSON

Retrieves invoice JSON from CII or UBL XML in finaX.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finaX/latest/actions/cii-or-ubl-to-json?connectionId=$CONNECTION_ID&file=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finaX/latest/actions/cii-or-ubl-to-json?${params}`, {
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
      "additionalSupportingDocuments": [
        {}
      ],
      "buyer": {},
      "buyerAccountingReference": "string",
      "buyerReference": "string",
      "contractReference": "string",
      "deliveryInformation": {},
      "despatchAdviceReference": "string",
      "documentLevelAllowances": [
        {}
      ],
      "documentLevelCharges": [
        {}
      ],
      "documentTotals": {},
      "extension": true,
      "invoiceCurrencyCode": "string",
      "invoicedObjectIdentifier": {},
      "invoiceIssueDate": "string",
      "invoiceLine": [
        {}
      ],
      "invoiceNote": [
        {}
      ],
      "invoiceNumber": "string",
      "invoiceTypeCode": 1,
      "payee": {},
      "paymentDueDate": "string",
      "paymentInstructions": {},
      "paymentTerms": "string",
      "precedingInvoiceReference": [
        {}
      ],
      "projectReference": "string",
      "purchaseOrderReference": "string",
      "receivingAdviceReference": "string",
      "salesOrderReference": "string",
      "seller": {},
      "sellerTaxRepresentativeParty": {},
      "tenderOrLotReference": "string",
      "thirdPartyPayment": [
        {}
      ],
      "validationMode": "string",
      "valueAddedTaxPointDate": "string",
      "valueAddedTaxPointDateCode": "string",
      "vatAccountingCurrencyCode": "string",
      "vatBreakdown": [
        {}
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [CII Or UBL To JSON action reference](actions/cii-or-ubl-to-json.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finaX/latest/actions/cii-or-ubl-to-json).

## CII Invoice Xml

Creates CII invoice XML from JSON in finaX.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finaX/latest/actions/cii-invoice-xml" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoice": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finaX/latest/actions/cii-invoice-xml', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoice": {}
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
      "xml": "string"
    }
  ],
  "meta": {}
}
```

See the full [CII Invoice Xml action reference](actions/cii-invoice-xml.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finaX/latest/actions/cii-invoice-xml).
