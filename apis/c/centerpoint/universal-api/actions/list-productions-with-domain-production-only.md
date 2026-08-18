# Centerpoint: List Productions With Domain Production Only



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-productions-with-domain-production-only
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-productions-with-domain-production-only?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-productions-with-domain-production-only?${params}`, {
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
| `updatedAfter` | string | no | Example: 2025-01-13 10:00:00 |
| `updatedBefore` | string | no |  |
| `include` | string | no |  |
| `filter[domain]` | string | no | Example: `production`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "archivedAt": {},
        "billedCompanyId": 1,
        "billedProfileId": {},
        "closedAt": {},
        "combinedInvoiceOptions": {
          "profitPerHour": 1,
          "view": "string"
        },
        "completedAt": {},
        "cost": 1,
        "createdAt": "string",
        "custom": {
          "calllback": {},
          "httpsgooglecom": {},
          "hyperlink": {},
          "temp": {},
          "test": {},
          "test1": {}
        },
        "customWithLabels": {
          "calllBack": {},
          "https://google": {
            "com": {}
          },
          "hyperlink": {},
          "tEMP": {},
          "test": {},
          "tEST": {}
        },
        "deletedAt": {},
        "description": {},
        "displayStatus": "string",
        "domain": "string",
        "dueAt": {},
        "dueDate": {},
        "dueDateHasTime": true,
        "endDate": {},
        "estimatedStartDate": {},
        "estimatorId": {},
        "exportStatus": "string",
        "forecasted": "string",
        "forecastedAt": {},
        "heldAt": {},
        "importId": {},
        "invoicedAt": {},
        "invoicePurchaseOrder": {},
        "isApprovalRequired": {},
        "laborTravelTotal": 1,
        "latestStageTransitionedAt": "string",
        "leadDeadAt": {},
        "leadOpenedAt": "string",
        "leadPendingAt": {},
        "leadQuotedAt": {},
        "leadSoldAt": {},
        "leadTypeId": {},
        "materialTotal": 1,
        "name": "Ava Chen",
        "nameNumber": {},
        "namePrefix": {},
        "openedAt": {},
        "opportunityType": "string",
        "options": {
          "contractorNTE": 1,
          "lumpSumSitebid": true,
          "measurement": 1,
          "notifications": "string",
          "nte": 1,
          "originalContractAmount": 1
        },
        "price": 1,
        "profileId": 1,
        "projectedCloseDate": {},
        "propertyId": 1,
        "propertyName": "Ava Chen",
        "recentActivity": "string",
        "scheduledAt": {},
        "serviceWorkflow": {
          "checkinName": "Ava Chen",
          "checkinNotes": "string",
          "checkoutName": "Ava Chen",
          "finalNotes": "string",
          "numTechs": 1,
          "opportunityId": 1,
          "signature": "string"
        },
        "startDate": {},
        "startedAt": {},
        "startTime": {},
        "status": "string",
        "totalInvoiced": 1,
        "type": {},
        "updatedAt": "string",
        "workProfileId": {},
        "workRate": 1,
        "workType": {}
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.archivedAt` | object |  |
| `attributes.billedCompanyId` | number |  |
| `attributes.billedProfileId` | object |  |
| `attributes.closedAt` | object |  |
| `attributes.combinedInvoiceOptions.profitPerHour` | number |  |
| `attributes.combinedInvoiceOptions.view` | string |  |
| `attributes.completedAt` | object |  |
| `attributes.cost` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.custom.calllback` | object |  |
| `attributes.custom.httpsgooglecom` | object |  |
| `attributes.custom.hyperlink` | object |  |
| `attributes.custom.temp` | object |  |
| `attributes.custom.test` | object |  |
| `attributes.custom.test1` | object |  |
| `attributes.customWithLabels.calllBack` | object |  |
| `attributes.customWithLabels.https://google.com` | object |  |
| `attributes.customWithLabels.hyperlink` | object |  |
| `attributes.customWithLabels.tEMP` | object |  |
| `attributes.customWithLabels.test` | object |  |
| `attributes.customWithLabels.tEST` | object |  |
| `attributes.deletedAt` | object |  |
| `attributes.description` | object |  |
| `attributes.displayStatus` | string |  |
| `attributes.domain` | string |  |
| `attributes.dueAt` | object |  |
| `attributes.dueDate` | object |  |
| `attributes.dueDateHasTime` | boolean |  |
| `attributes.endDate` | object |  |
| `attributes.estimatedStartDate` | object |  |
| `attributes.estimatorId` | object |  |
| `attributes.exportStatus` | string |  |
| `attributes.forecasted` | string |  |
| `attributes.forecastedAt` | object |  |
| `attributes.heldAt` | object |  |
| `attributes.importId` | object |  |
| `attributes.invoicedAt` | object |  |
| `attributes.invoicePurchaseOrder` | object |  |
| `attributes.isApprovalRequired` | object |  |
| `attributes.laborTravelTotal` | number |  |
| `attributes.latestStageTransitionedAt` | string |  |
| `attributes.leadDeadAt` | object |  |
| `attributes.leadOpenedAt` | string |  |
| `attributes.leadPendingAt` | object |  |
| `attributes.leadQuotedAt` | object |  |
| `attributes.leadSoldAt` | object |  |
| `attributes.leadTypeId` | object |  |
| `attributes.materialTotal` | number |  |
| `attributes.name` | string |  |
| `attributes.nameNumber` | object |  |
| `attributes.namePrefix` | object |  |
| `attributes.openedAt` | object |  |
| `attributes.opportunityType` | string |  |
| `attributes.options.contractorNTE` | number |  |
| `attributes.options.lumpSumSitebid` | boolean |  |
| `attributes.options.measurement` | number |  |
| `attributes.options.notifications` | string |  |
| `attributes.options.nte` | number |  |
| `attributes.options.originalContractAmount` | number |  |
| `attributes.price` | number |  |
| `attributes.profileId` | number |  |
| `attributes.projectedCloseDate` | object |  |
| `attributes.propertyId` | number |  |
| `attributes.propertyName` | string |  |
| `attributes.recentActivity` | string |  |
| `attributes.scheduledAt` | object |  |
| `attributes.serviceWorkflow.checkinName` | string |  |
| `attributes.serviceWorkflow.checkinNotes` | string |  |
| `attributes.serviceWorkflow.checkoutName` | string |  |
| `attributes.serviceWorkflow.finalNotes` | string |  |
| `attributes.serviceWorkflow.numTechs` | number |  |
| `attributes.serviceWorkflow.opportunityId` | number |  |
| `attributes.serviceWorkflow.signature` | string |  |
| `attributes.startDate` | object |  |
| `attributes.startedAt` | object |  |
| `attributes.startTime` | object |  |
| `attributes.status` | string |  |
| `attributes.totalInvoiced` | number |  |
| `attributes.type` | object |  |
| `attributes.updatedAt` | string |  |
| `attributes.workProfileId` | object |  |
| `attributes.workRate` | number |  |
| `attributes.workType` | object |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET productions` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-productions-with-domain-production-only.md) for the provider-specific parameters and requirements.

