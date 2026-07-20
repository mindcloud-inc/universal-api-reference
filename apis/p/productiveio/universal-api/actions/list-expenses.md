# Productive.io: List Expenses

Retrieves expenses from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-expenses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-expenses?${params}`, {
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
        "amountDefault": 1,
        "amountNormalized": 1,
        "amountWithTax": 1,
        "amountWithTaxDefault": 1,
        "amountWithTaxNormalized": 1,
        "approved": true,
        "approvedAt": "string",
        "billableAmount": 1,
        "billableAmountDefault": 1,
        "billableAmountNormalized": 1,
        "companyReferenceId": "string",
        "createdAt": "string",
        "currency": "string",
        "currencyDefault": "string",
        "currencyNormalized": "string",
        "customFields": "string",
        "date": "string",
        "deletedAt": "string",
        "draft": true,
        "exchangeDate": "string",
        "exchangeRate": "string",
        "exchangeRateNormalized": "string",
        "exported": true,
        "exportedAt": "string",
        "exportId": "string",
        "exportIntegrationTypeId": "string",
        "exportUrl": "https://example.com",
        "externalPaymentId": "string",
        "invoiced": true,
        "lineItemsCount": 1,
        "markup": "string",
        "name": "Ava Chen",
        "paidOn": "string",
        "payOn": "string",
        "position": 1,
        "profit": 1,
        "profitDefault": 1,
        "profitNormalized": 1,
        "quantity": "string",
        "quantityReceived": "string",
        "recognizedRevenue": 1,
        "recognizedRevenueDefault": 1,
        "recognizedRevenueNormalized": 1,
        "reimbursable": true,
        "reimbursedOn": "string",
        "rejected": true,
        "rejectedAt": "string",
        "rejectedReason": "string",
        "taxInclusion": true,
        "totalAmount": 1,
        "totalAmountDefault": 1,
        "totalAmountNormalized": 1,
        "totalAmountWithTax": 1,
        "totalAmountWithTaxDefault": 1,
        "totalAmountWithTaxNormalized": 1
      },
      "id": "string",
      "relationships": {
        "approvalStatuses": {
          "meta": {
            "included": true
          }
        },
        "approver": {
          "meta": {
            "included": true
          }
        },
        "attachment": {
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
        "deal": {
          "meta": {
            "included": true
          }
        },
        "invoiceAttribution": {
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
        "person": {
          "meta": {
            "included": true
          }
        },
        "purchaseOrder": {
          "meta": {
            "included": true
          }
        },
        "rejecter": {
          "meta": {
            "included": true
          }
        },
        "service": {
          "meta": {
            "included": true
          }
        },
        "serviceType": {
          "meta": {
            "included": true
          }
        },
        "taxRate": {
          "meta": {
            "included": true
          }
        },
        "vendor": {
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
| `attributes.amountDefault` | number |  |
| `attributes.amountNormalized` | number |  |
| `attributes.amountWithTax` | number |  |
| `attributes.amountWithTaxDefault` | number |  |
| `attributes.amountWithTaxNormalized` | number |  |
| `attributes.approved` | boolean |  |
| `attributes.approvedAt` | string |  |
| `attributes.billableAmount` | number |  |
| `attributes.billableAmountDefault` | number |  |
| `attributes.billableAmountNormalized` | number |  |
| `attributes.companyReferenceId` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.currency` | string |  |
| `attributes.currencyDefault` | string |  |
| `attributes.currencyNormalized` | string |  |
| `attributes.customFields` | string |  |
| `attributes.date` | string |  |
| `attributes.deletedAt` | string |  |
| `attributes.draft` | boolean |  |
| `attributes.exchangeDate` | string |  |
| `attributes.exchangeRate` | string |  |
| `attributes.exchangeRateNormalized` | string |  |
| `attributes.exported` | boolean |  |
| `attributes.exportedAt` | string |  |
| `attributes.exportId` | string |  |
| `attributes.exportIntegrationTypeId` | string |  |
| `attributes.exportUrl` | string |  |
| `attributes.externalPaymentId` | string |  |
| `attributes.invoiced` | boolean |  |
| `attributes.lineItemsCount` | number |  |
| `attributes.markup` | string |  |
| `attributes.name` | string |  |
| `attributes.paidOn` | string |  |
| `attributes.payOn` | string |  |
| `attributes.position` | number |  |
| `attributes.profit` | number |  |
| `attributes.profitDefault` | number |  |
| `attributes.profitNormalized` | number |  |
| `attributes.quantity` | string |  |
| `attributes.quantityReceived` | string |  |
| `attributes.recognizedRevenue` | number |  |
| `attributes.recognizedRevenueDefault` | number |  |
| `attributes.recognizedRevenueNormalized` | number |  |
| `attributes.reimbursable` | boolean |  |
| `attributes.reimbursedOn` | string |  |
| `attributes.rejected` | boolean |  |
| `attributes.rejectedAt` | string |  |
| `attributes.rejectedReason` | string |  |
| `attributes.taxInclusion` | boolean |  |
| `attributes.totalAmount` | number |  |
| `attributes.totalAmountDefault` | number |  |
| `attributes.totalAmountNormalized` | number |  |
| `attributes.totalAmountWithTax` | number |  |
| `attributes.totalAmountWithTaxDefault` | number |  |
| `attributes.totalAmountWithTaxNormalized` | number |  |
| `id` | string |  |
| `relationships.approvalStatuses.meta.included` | boolean |  |
| `relationships.approver.meta.included` | boolean |  |
| `relationships.attachment.meta.included` | boolean |  |
| `relationships.creator.meta.included` | boolean |  |
| `relationships.customFieldAttachments.meta.included` | boolean |  |
| `relationships.customFieldPeople.meta.included` | boolean |  |
| `relationships.deal.meta.included` | boolean |  |
| `relationships.invoiceAttribution.meta.included` | boolean |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.person.meta.included` | boolean |  |
| `relationships.purchaseOrder.meta.included` | boolean |  |
| `relationships.rejecter.meta.included` | boolean |  |
| `relationships.service.meta.included` | boolean |  |
| `relationships.serviceType.meta.included` | boolean |  |
| `relationships.taxRate.meta.included` | boolean |  |
| `relationships.vendor.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /expenses` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

