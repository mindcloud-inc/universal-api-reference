# Productive.io: List Deals

Retrieves deals from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-deals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-deals?${params}`, {
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
        "accessToDeal": true,
        "amountCredited": 1,
        "amountCreditedDefault": 1,
        "amountCreditedNormalized": 1,
        "billableTime": 1,
        "budget": true,
        "budgetedTime": 1,
        "budgetTotal": 1,
        "budgetTotalDefault": 1,
        "budgetTotalNormalized": 1,
        "budgetUsed": 1,
        "budgetUsedDefault": 1,
        "budgetUsedNormalized": 1,
        "budgetWarning": "string",
        "clientAccess": true,
        "closedAt": "string",
        "colorId": "string",
        "cost": 1,
        "costDefault": 1,
        "costNormalized": 1,
        "createdAt": "string",
        "currency": "string",
        "currencyDefault": "string",
        "currencyNormalized": "string",
        "customFields": "string",
        "date": "string",
        "daysInCurrentStage": 1,
        "daysSinceCreated": 1,
        "daysSinceLastActivity": 1,
        "dealNumber": "string",
        "dealTypeId": 1,
        "deletedAt": "string",
        "deliveredOn": "string",
        "discount": "string",
        "draftInvoiced": 1,
        "draftInvoicedDefault": 1,
        "draftInvoicedNormalized": 1,
        "editorConfig": "string",
        "emailKey": "ava@example.com",
        "endDate": "string",
        "estimatedTime": 1,
        "exchangeDate": "string",
        "exchangeRate": "string",
        "expense": 1,
        "expenseApproval": true,
        "expenseDefault": 1,
        "expenseNormalized": 1,
        "externalId": "string",
        "externalSync": true,
        "footer": "string",
        "footerInterpolated": "string",
        "invoiced": 1,
        "invoicedDefault": 1,
        "invoicedNormalized": 1,
        "lastActivityAt": "string",
        "lostComment": "string",
        "manDayMinutes": 1,
        "manualInvoicingStatusId": 1,
        "manuallyInvoiced": 1,
        "manuallyInvoicedDefault": 1,
        "manuallyInvoicedNormalized": 1,
        "name": "Ava Chen",
        "note": "string",
        "noteInterpolated": "string",
        "number": "string",
        "originDealId": "string",
        "pendingInvoicing": 1,
        "pendingInvoicingDefault": 1,
        "pendingInvoicingNormalized": 1,
        "position": 1,
        "previousProbability": "string",
        "probability": 1,
        "profit": 1,
        "profitDefault": 1,
        "profitMargin": "string",
        "profitMarginDefault": "string",
        "profitMarginNormalized": "string",
        "profitNormalized": 1,
        "projectedRevenue": 1,
        "projectedRevenueDefault": 1,
        "projectedRevenueNormalized": 1,
        "proposalFooter": "string",
        "proposalFooterInterpolated": "string",
        "proposalNote": "string",
        "proposalNoteInterpolated": "string",
        "purchaseOrderNumber": "string",
        "revenue": 1,
        "revenueDefault": 1,
        "revenueDistributionMethod": "string",
        "revenueDistributionType": "string",
        "revenueNormalized": 1,
        "roundingIntervalId": "string",
        "roundingMethodId": 1,
        "salesClosedAt": "string",
        "salesClosedOn": "string",
        "salesStatusUpdatedAt": "string",
        "sampleData": true,
        "servicesRevenue": 1,
        "servicesRevenueDefault": 1,
        "servicesRevenueNormalized": 1,
        "serviceTypeRestrictedTracking": true,
        "suffix": "string",
        "tagList": [
          "string"
        ],
        "timeApproval": true,
        "timeToClose": "string",
        "todoCount": 1,
        "todoDueDate": "string",
        "trackingTypeId": 1,
        "validateExpenseWhenClosing": true,
        "workedTime": 1
      },
      "id": "string",
      "relationships": {
        "approvalPolicyAssignment": {
          "meta": {
            "included": true
          }
        },
        "automaticInvoicingRule": {
          "meta": {
            "included": true
          }
        },
        "company": {
          "meta": {
            "included": true
          }
        },
        "contact": {
          "meta": {
            "included": true
          }
        },
        "contract": {
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
        "dealStatus": {
          "meta": {
            "included": true
          }
        },
        "documentType": {
          "meta": {
            "included": true
          }
        },
        "expenseApprovalWorkflow": {
          "meta": {
            "included": true
          }
        },
        "invoiceTemplate": {
          "meta": {
            "included": true
          }
        },
        "lostReason": {
          "meta": {
            "included": true
          }
        },
        "nextTodo": {
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
        "originDeal": {
          "meta": {
            "included": true
          }
        },
        "pipeline": {
          "meta": {
            "included": true
          }
        },
        "project": {
          "meta": {
            "included": true
          }
        },
        "proposalDocumentType": {
          "meta": {
            "included": true
          }
        },
        "responsible": {
          "meta": {
            "included": true
          }
        },
        "subsidiary": {
          "meta": {
            "included": true
          }
        },
        "taxRate": {
          "meta": {
            "included": true
          }
        },
        "template": {
          "meta": {
            "included": true
          }
        },
        "timeApprovalWorkflow": {
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
| `attributes.accessToDeal` | boolean |  |
| `attributes.amountCredited` | number |  |
| `attributes.amountCreditedDefault` | number |  |
| `attributes.amountCreditedNormalized` | number |  |
| `attributes.billableTime` | number |  |
| `attributes.budget` | boolean |  |
| `attributes.budgetedTime` | number |  |
| `attributes.budgetTotal` | number |  |
| `attributes.budgetTotalDefault` | number |  |
| `attributes.budgetTotalNormalized` | number |  |
| `attributes.budgetUsed` | number |  |
| `attributes.budgetUsedDefault` | number |  |
| `attributes.budgetUsedNormalized` | number |  |
| `attributes.budgetWarning` | string |  |
| `attributes.clientAccess` | boolean |  |
| `attributes.closedAt` | string |  |
| `attributes.colorId` | string |  |
| `attributes.cost` | number |  |
| `attributes.costDefault` | number |  |
| `attributes.costNormalized` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.currency` | string |  |
| `attributes.currencyDefault` | string |  |
| `attributes.currencyNormalized` | string |  |
| `attributes.customFields` | string |  |
| `attributes.date` | string |  |
| `attributes.daysInCurrentStage` | number |  |
| `attributes.daysSinceCreated` | number |  |
| `attributes.daysSinceLastActivity` | number |  |
| `attributes.dealNumber` | string |  |
| `attributes.dealTypeId` | number |  |
| `attributes.deletedAt` | string |  |
| `attributes.deliveredOn` | string |  |
| `attributes.discount` | string |  |
| `attributes.draftInvoiced` | number |  |
| `attributes.draftInvoicedDefault` | number |  |
| `attributes.draftInvoicedNormalized` | number |  |
| `attributes.editorConfig` | string |  |
| `attributes.emailKey` | string |  |
| `attributes.endDate` | string |  |
| `attributes.estimatedTime` | number |  |
| `attributes.exchangeDate` | string |  |
| `attributes.exchangeRate` | string |  |
| `attributes.expense` | number |  |
| `attributes.expenseApproval` | boolean |  |
| `attributes.expenseDefault` | number |  |
| `attributes.expenseNormalized` | number |  |
| `attributes.externalId` | string |  |
| `attributes.externalSync` | boolean |  |
| `attributes.footer` | string |  |
| `attributes.footerInterpolated` | string |  |
| `attributes.invoiced` | number |  |
| `attributes.invoicedDefault` | number |  |
| `attributes.invoicedNormalized` | number |  |
| `attributes.lastActivityAt` | string |  |
| `attributes.lostComment` | string |  |
| `attributes.manDayMinutes` | number |  |
| `attributes.manualInvoicingStatusId` | number |  |
| `attributes.manuallyInvoiced` | number |  |
| `attributes.manuallyInvoicedDefault` | number |  |
| `attributes.manuallyInvoicedNormalized` | number |  |
| `attributes.name` | string |  |
| `attributes.note` | string |  |
| `attributes.noteInterpolated` | string |  |
| `attributes.number` | string |  |
| `attributes.originDealId` | string |  |
| `attributes.pendingInvoicing` | number |  |
| `attributes.pendingInvoicingDefault` | number |  |
| `attributes.pendingInvoicingNormalized` | number |  |
| `attributes.position` | number |  |
| `attributes.previousProbability` | string |  |
| `attributes.probability` | number |  |
| `attributes.profit` | number |  |
| `attributes.profitDefault` | number |  |
| `attributes.profitMargin` | string |  |
| `attributes.profitMarginDefault` | string |  |
| `attributes.profitMarginNormalized` | string |  |
| `attributes.profitNormalized` | number |  |
| `attributes.projectedRevenue` | number |  |
| `attributes.projectedRevenueDefault` | number |  |
| `attributes.projectedRevenueNormalized` | number |  |
| `attributes.proposalFooter` | string |  |
| `attributes.proposalFooterInterpolated` | string |  |
| `attributes.proposalNote` | string |  |
| `attributes.proposalNoteInterpolated` | string |  |
| `attributes.purchaseOrderNumber` | string |  |
| `attributes.revenue` | number |  |
| `attributes.revenueDefault` | number |  |
| `attributes.revenueDistributionMethod` | string |  |
| `attributes.revenueDistributionType` | string |  |
| `attributes.revenueNormalized` | number |  |
| `attributes.roundingIntervalId` | string |  |
| `attributes.roundingMethodId` | number |  |
| `attributes.salesClosedAt` | string |  |
| `attributes.salesClosedOn` | string |  |
| `attributes.salesStatusUpdatedAt` | string |  |
| `attributes.sampleData` | boolean |  |
| `attributes.servicesRevenue` | number |  |
| `attributes.servicesRevenueDefault` | number |  |
| `attributes.servicesRevenueNormalized` | number |  |
| `attributes.serviceTypeRestrictedTracking` | boolean |  |
| `attributes.suffix` | string |  |
| `attributes.tagList` | array<string> |  |
| `attributes.timeApproval` | boolean |  |
| `attributes.timeToClose` | string |  |
| `attributes.todoCount` | number |  |
| `attributes.todoDueDate` | string |  |
| `attributes.trackingTypeId` | number |  |
| `attributes.validateExpenseWhenClosing` | boolean |  |
| `attributes.workedTime` | number |  |
| `id` | string |  |
| `relationships.approvalPolicyAssignment.meta.included` | boolean |  |
| `relationships.automaticInvoicingRule.meta.included` | boolean |  |
| `relationships.company.meta.included` | boolean |  |
| `relationships.contact.meta.included` | boolean |  |
| `relationships.contract.meta.included` | boolean |  |
| `relationships.creator.meta.included` | boolean |  |
| `relationships.customFieldAttachments.meta.included` | boolean |  |
| `relationships.customFieldPeople.meta.included` | boolean |  |
| `relationships.dealStatus.meta.included` | boolean |  |
| `relationships.documentType.meta.included` | boolean |  |
| `relationships.expenseApprovalWorkflow.meta.included` | boolean |  |
| `relationships.invoiceTemplate.meta.included` | boolean |  |
| `relationships.lostReason.meta.included` | boolean |  |
| `relationships.nextTodo.meta.included` | boolean |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.originDeal.meta.included` | boolean |  |
| `relationships.pipeline.meta.included` | boolean |  |
| `relationships.project.meta.included` | boolean |  |
| `relationships.proposalDocumentType.meta.included` | boolean |  |
| `relationships.responsible.meta.included` | boolean |  |
| `relationships.subsidiary.meta.included` | boolean |  |
| `relationships.taxRate.meta.included` | boolean |  |
| `relationships.template.meta.included` | boolean |  |
| `relationships.timeApprovalWorkflow.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /deals` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deals.md) for the provider-specific parameters and requirements.

