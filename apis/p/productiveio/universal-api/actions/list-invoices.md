# Productive.io: List Invoices

Retrieves invoices from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "amount": 1,
        "amountCredited": 1,
        "amountCreditedDefault": 1,
        "amountCreditedNormalized": 1,
        "amountCreditedWithTax": 1,
        "amountCreditedWithTaxDefault": 1,
        "amountCreditedWithTaxNormalized": 1,
        "amountDefault": 1,
        "amountNormalized": 1,
        "amountPaid": 1,
        "amountPaidDefault": 1,
        "amountPaidNormalized": 1,
        "amountTax": 1,
        "amountTaxDefault": 1,
        "amountTaxNormalized": 1,
        "amountUnpaid": 1,
        "amountUnpaidDefault": 1,
        "amountUnpaidNormalized": 1,
        "amountWithTax": 1,
        "amountWithTaxDefault": 1,
        "amountWithTaxNormalized": 1,
        "amountWrittenOff": 1,
        "amountWrittenOffDefault": 1,
        "amountWrittenOffNormalized": 1,
        "bankAccountDetails": "string",
        "companyReferenceId": "string",
        "createdAt": "string",
        "credited": true,
        "currency": "string",
        "currencyDefault": "string",
        "currencyNormalized": "string",
        "customFields": "string",
        "deletedAt": "string",
        "deliveryOn": "string",
        "discount": "string",
        "emailKey": "ava@example.com",
        "exchangeDate": "string",
        "exchangeRate": "string",
        "exported": true,
        "exportedAt": "string",
        "exportId": "string",
        "exportIntegrationTypeId": "string",
        "exportInvoiceUrl": "https://example.com",
        "finalizedAt": "string",
        "finalizedOn": "string",
        "footer": "string",
        "footerInterpolated": "string",
        "invoicedOn": "string",
        "invoiceTemplateId": "string",
        "invoiceTypeId": 1,
        "lastActivityAt": "string",
        "lineItemTax": true,
        "note": "string",
        "noteInterpolated": "string",
        "number": "string",
        "paidOn": "string",
        "paymentTerms": 1,
        "payOn": "string",
        "payOnRelative": true,
        "purchaseOrderNumber": "string",
        "sampleData": true,
        "sentOn": "string",
        "subject": "string",
        "tagList": [
          "string"
        ],
        "tax1Name": "Ava Chen",
        "tax1Value": "string",
        "tax2Name": "Ava Chen",
        "tax2Value": "string",
        "updatedAt": "string"
      },
      "id": "string",
      "relationships": {
        "attachment": {
          "meta": {
            "included": true
          }
        },
        "bankAccount": {
          "meta": {
            "included": true
          }
        },
        "billFrom": {
          "meta": {
            "included": true
          }
        },
        "billTo": {
          "meta": {
            "included": true
          }
        },
        "company": {
          "meta": {
            "included": true
          }
        },
        "creator": {
          "meta": {
            "included": true
          }
        },
        "customFieldAttachments": {
          "meta": {
            "included": true
          }
        },
        "customFieldPeople": {
          "meta": {
            "included": true
          }
        },
        "documentType": {
          "meta": {
            "included": true
          }
        },
        "invoiceAttributions": {
          "meta": {
            "included": true
          }
        },
        "issuer": {
          "meta": {
            "included": true
          }
        },
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "parentInvoice": {
          "meta": {
            "included": true
          }
        },
        "subsidiary": {
          "meta": {
            "included": true
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.amount` | number |  |
| `attributes.amountCredited` | number |  |
| `attributes.amountCreditedDefault` | number |  |
| `attributes.amountCreditedNormalized` | number |  |
| `attributes.amountCreditedWithTax` | number |  |
| `attributes.amountCreditedWithTaxDefault` | number |  |
| `attributes.amountCreditedWithTaxNormalized` | number |  |
| `attributes.amountDefault` | number |  |
| `attributes.amountNormalized` | number |  |
| `attributes.amountPaid` | number |  |
| `attributes.amountPaidDefault` | number |  |
| `attributes.amountPaidNormalized` | number |  |
| `attributes.amountTax` | number |  |
| `attributes.amountTaxDefault` | number |  |
| `attributes.amountTaxNormalized` | number |  |
| `attributes.amountUnpaid` | number |  |
| `attributes.amountUnpaidDefault` | number |  |
| `attributes.amountUnpaidNormalized` | number |  |
| `attributes.amountWithTax` | number |  |
| `attributes.amountWithTaxDefault` | number |  |
| `attributes.amountWithTaxNormalized` | number |  |
| `attributes.amountWrittenOff` | number |  |
| `attributes.amountWrittenOffDefault` | number |  |
| `attributes.amountWrittenOffNormalized` | number |  |
| `attributes.bankAccountDetails` | string |  |
| `attributes.companyReferenceId` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.credited` | boolean |  |
| `attributes.currency` | string |  |
| `attributes.currencyDefault` | string |  |
| `attributes.currencyNormalized` | string |  |
| `attributes.customFields` | string |  |
| `attributes.deletedAt` | string |  |
| `attributes.deliveryOn` | string |  |
| `attributes.discount` | string |  |
| `attributes.emailKey` | string |  |
| `attributes.exchangeDate` | string |  |
| `attributes.exchangeRate` | string |  |
| `attributes.exported` | boolean |  |
| `attributes.exportedAt` | string |  |
| `attributes.exportId` | string |  |
| `attributes.exportIntegrationTypeId` | string |  |
| `attributes.exportInvoiceUrl` | string |  |
| `attributes.finalizedAt` | string |  |
| `attributes.finalizedOn` | string |  |
| `attributes.footer` | string |  |
| `attributes.footerInterpolated` | string |  |
| `attributes.invoicedOn` | string |  |
| `attributes.invoiceTemplateId` | string |  |
| `attributes.invoiceTypeId` | number |  |
| `attributes.lastActivityAt` | string |  |
| `attributes.lineItemTax` | boolean |  |
| `attributes.note` | string |  |
| `attributes.noteInterpolated` | string |  |
| `attributes.number` | string |  |
| `attributes.paidOn` | string |  |
| `attributes.paymentTerms` | number |  |
| `attributes.payOn` | string |  |
| `attributes.payOnRelative` | boolean |  |
| `attributes.purchaseOrderNumber` | string |  |
| `attributes.sampleData` | boolean |  |
| `attributes.sentOn` | string |  |
| `attributes.subject` | string |  |
| `attributes.tagList` | array<string> |  |
| `attributes.tax1Name` | string |  |
| `attributes.tax1Value` | string |  |
| `attributes.tax2Name` | string |  |
| `attributes.tax2Value` | string |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `relationships.attachment.meta.included` | boolean |  |
| `relationships.bankAccount.meta.included` | boolean |  |
| `relationships.billFrom.meta.included` | boolean |  |
| `relationships.billTo.meta.included` | boolean |  |
| `relationships.company.meta.included` | boolean |  |
| `relationships.creator.meta.included` | boolean |  |
| `relationships.customFieldAttachments.meta.included` | boolean |  |
| `relationships.customFieldPeople.meta.included` | boolean |  |
| `relationships.documentType.meta.included` | boolean |  |
| `relationships.invoiceAttributions.meta.included` | boolean |  |
| `relationships.issuer.meta.included` | boolean |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.parentInvoice.meta.included` | boolean |  |
| `relationships.subsidiary.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /invoices` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

