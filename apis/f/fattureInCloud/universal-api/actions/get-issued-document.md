# Fatture in Cloud: Get Issued Document

Retrieves an issued document from Fatture in Cloud.

```
GET https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/get-issued-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/get-issued-document?connectionId=$CONNECTION_ID&companyId=1&documentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1",
  "documentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/get-issued-document?${params}`, {
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
| `companyId` | number | yes | The ID of the company. |
| `documentId` | number | yes | The ID of the document. |
| `fields` | string | no | List of comma-separated fields. |
| `fieldset` | list | no | Name of the fieldset. One of: `basic`, `detailed`, `fic_view`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accompanyingInvoice": true,
      "amountCassa": 1,
      "amountDueDiscount": 1,
      "amountGross": 1,
      "amountNet": 1,
      "amountOtherWithholdingTax": 1,
      "amountRivalsa": 1,
      "amountVat": 1,
      "amountWithholdingTax": 1,
      "attachmentUrl": "https://example.com",
      "cassa": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": {
        "exchangeRate": "string",
        "id": "string",
        "symbol": "string"
      },
      "date": "2026-05-07T12:00:00.000Z",
      "deliveryNote": true,
      "eInvoice": true,
      "entity": {
        "addressCity": "string",
        "addressExtra": "string",
        "addressPostalCode": "string",
        "addressProvince": "string",
        "addressStreet": "string",
        "certifiedEmail": "ava@example.com",
        "country": "string",
        "eiCode": "string",
        "id": 1,
        "name": "Ava Chen",
        "taxCode": "string",
        "vatNumber": "string"
      },
      "hasTsPayPendingPayment": true,
      "hMargins": 1,
      "id": 1,
      "isMarked": true,
      "itemsList": [
        {
          "applyWithholdingTaxes": true,
          "category": "string",
          "code": "string",
          "description": "string",
          "discount": 1,
          "discountHighlight": true,
          "grossPrice": 1,
          "id": 1,
          "inDn": true,
          "measure": "string",
          "name": "Ava Chen",
          "netPrice": 1,
          "notTaxable": true,
          "productId": 1,
          "qty": 1,
          "stock": true,
          "vat": {
            "description": "string",
            "id": 1,
            "value": 1
          }
        }
      ],
      "language": {
        "code": "string",
        "name": "Ava Chen"
      },
      "locked": true,
      "nextDueDate": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "number": 1,
      "numeration": "string",
      "otherWithholdingTax": 1,
      "paymentMethod": {
        "id": 1,
        "name": "Ava Chen"
      },
      "paymentsList": [
        {
          "amount": 1,
          "dueDate": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "paymentTerms": {
            "days": 1,
            "type": "string"
          },
          "status": "string"
        }
      ],
      "priceListId": "string",
      "rcCenter": "string",
      "rivalsa": 1,
      "showNotificationButton": true,
      "showPaymentMethod": true,
      "showPayments": true,
      "showTotals": "string",
      "showTspayButton": true,
      "stampDuty": 1,
      "subject": "string",
      "template": {
        "id": 1,
        "name": "Ava Chen"
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "useGrossPrices": true,
      "useSplitPayment": true,
      "visibleSubject": "string",
      "vMargins": 1,
      "withholdingTax": 1,
      "withholdingTaxTaxable": 1,
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accompanyingInvoice` | boolean |  |
| `amountCassa` | number |  |
| `amountDueDiscount` | number |  |
| `amountGross` | number |  |
| `amountNet` | number |  |
| `amountOtherWithholdingTax` | number |  |
| `amountRivalsa` | number |  |
| `amountVat` | number |  |
| `amountWithholdingTax` | number |  |
| `attachmentUrl` | string |  |
| `cassa` | number |  |
| `createdAt` | date |  |
| `currency.exchangeRate` | string |  |
| `currency.id` | string |  |
| `currency.symbol` | string |  |
| `date` | date |  |
| `deliveryNote` | boolean |  |
| `eInvoice` | boolean |  |
| `entity.addressCity` | string |  |
| `entity.addressExtra` | string |  |
| `entity.addressPostalCode` | string |  |
| `entity.addressProvince` | string |  |
| `entity.addressStreet` | string |  |
| `entity.certifiedEmail` | string |  |
| `entity.country` | string |  |
| `entity.eiCode` | string |  |
| `entity.id` | number |  |
| `entity.name` | string |  |
| `entity.taxCode` | string |  |
| `entity.vatNumber` | string |  |
| `hasTsPayPendingPayment` | boolean |  |
| `hMargins` | number |  |
| `id` | number |  |
| `isMarked` | boolean |  |
| `itemsList[].applyWithholdingTaxes` | boolean |  |
| `itemsList[].category` | string |  |
| `itemsList[].code` | string |  |
| `itemsList[].description` | string |  |
| `itemsList[].discount` | number |  |
| `itemsList[].discountHighlight` | boolean |  |
| `itemsList[].grossPrice` | number |  |
| `itemsList[].id` | number |  |
| `itemsList[].inDn` | boolean |  |
| `itemsList[].measure` | string |  |
| `itemsList[].name` | string |  |
| `itemsList[].netPrice` | number |  |
| `itemsList[].notTaxable` | boolean |  |
| `itemsList[].productId` | number |  |
| `itemsList[].qty` | number |  |
| `itemsList[].stock` | boolean |  |
| `itemsList[].vat.description` | string |  |
| `itemsList[].vat.id` | number |  |
| `itemsList[].vat.value` | number |  |
| `language.code` | string |  |
| `language.name` | string |  |
| `locked` | boolean |  |
| `nextDueDate` | date |  |
| `notes` | string |  |
| `number` | number |  |
| `numeration` | string |  |
| `otherWithholdingTax` | number |  |
| `paymentMethod.id` | number |  |
| `paymentMethod.name` | string |  |
| `paymentsList[].amount` | number |  |
| `paymentsList[].dueDate` | date |  |
| `paymentsList[].id` | number |  |
| `paymentsList[].paymentTerms.days` | number |  |
| `paymentsList[].paymentTerms.type` | string |  |
| `paymentsList[].status` | string |  |
| `priceListId` | string |  |
| `rcCenter` | string |  |
| `rivalsa` | number |  |
| `showNotificationButton` | boolean |  |
| `showPaymentMethod` | boolean |  |
| `showPayments` | boolean |  |
| `showTotals` | string |  |
| `showTspayButton` | boolean |  |
| `stampDuty` | number |  |
| `subject` | string |  |
| `template.id` | number |  |
| `template.name` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `useGrossPrices` | boolean |  |
| `useSplitPayment` | boolean |  |
| `visibleSubject` | string |  |
| `vMargins` | number |  |
| `withholdingTax` | number |  |
| `withholdingTaxTaxable` | number |  |
| `year` | number |  |

## Native endpoint

Through the native Fatture in Cloud API, this operation is `GET /c/:company_id/issued_documents/:document_id` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issued-document.md) for the provider-specific parameters and requirements.

