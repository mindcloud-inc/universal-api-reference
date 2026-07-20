# finaX: CII Or UBL To JSON

Retrieves invoice JSON from CII or UBL XML in finaX.

```
GET https://connect.mindcloud.co/v1/universal/finaX/latest/actions/cii-or-ubl-to-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a finaX `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Invoice XML file. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalSupportingDocuments` | array<object> |  |
| `buyer` | object |  |
| `buyerAccountingReference` | string |  |
| `buyerReference` | string |  |
| `contractReference` | string |  |
| `deliveryInformation` | object |  |
| `despatchAdviceReference` | string |  |
| `documentLevelAllowances` | array<object> |  |
| `documentLevelCharges` | array<object> |  |
| `documentTotals` | object |  |
| `extension` | boolean |  |
| `invoiceCurrencyCode` | string |  |
| `invoicedObjectIdentifier` | object |  |
| `invoiceIssueDate` | string |  |
| `invoiceLine` | array<object> |  |
| `invoiceNote` | array<object> |  |
| `invoiceNumber` | string |  |
| `invoiceTypeCode` | number |  |
| `payee` | object |  |
| `paymentDueDate` | string |  |
| `paymentInstructions` | object |  |
| `paymentTerms` | string |  |
| `precedingInvoiceReference` | array<object> |  |
| `projectReference` | string |  |
| `purchaseOrderReference` | string |  |
| `receivingAdviceReference` | string |  |
| `salesOrderReference` | string |  |
| `seller` | object |  |
| `sellerTaxRepresentativeParty` | object |  |
| `tenderOrLotReference` | string |  |
| `thirdPartyPayment` | array<object> |  |
| `validationMode` | string |  |
| `valueAddedTaxPointDate` | string |  |
| `valueAddedTaxPointDateCode` | string |  |
| `vatAccountingCurrencyCode` | string |  |
| `vatBreakdown` | array<object> |  |
| `version` | string |  |

## Native endpoint

Through the native finaX API, this operation is `POST /v1/json/xml/` (base URL `https://api.finax.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cii-or-ubl-to-json.md) for the provider-specific parameters and requirements.

