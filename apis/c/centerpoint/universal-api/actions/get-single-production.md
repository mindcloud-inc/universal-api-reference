# Centerpoint: Get Production



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-production
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-production?connectionId=$CONNECTION_ID&PRODUCTION_ID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "PRODUCTION_ID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-production?${params}`, {
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
| `PRODUCTION_ID` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[companies]` | string | no | Optional fields companies query parameter. |
| `fields[employees]` | string | no | Optional fields employees query parameter. |
| `fields[profiles]` | string | no | Optional fields profiles query parameter. |
| `fields[productionDays]` | string | no | Optional fields production days query parameter. |
| `fields[properties]` | string | no | Optional fields properties query parameter. |
| `include` | string | no | Optional include query parameter. |

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
        "customWithLabels": [
          {}
        ],
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
        "importId": "string",
        "invoicedAt": {},
        "invoicePurchaseOrder": {},
        "isApprovalRequired": {},
        "laborTravelTotal": 1,
        "latestPaidDate": {},
        "latestStageTransitionedAt": "string",
        "leadDeadAt": {},
        "leadOpenedAt": "string",
        "leadPendingAt": "string",
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
          "importBatchId": 1,
          "originalContractAmount": 1
        },
        "price": 1,
        "profileId": {},
        "projectedCloseDate": {},
        "propertyId": 1,
        "propertyName": "Ava Chen",
        "recentActivity": "string",
        "scheduledAt": {},
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
| `attributes.customWithLabels` | array<object> |  |
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
| `attributes.importId` | string |  |
| `attributes.invoicedAt` | object |  |
| `attributes.invoicePurchaseOrder` | object |  |
| `attributes.isApprovalRequired` | object |  |
| `attributes.laborTravelTotal` | number |  |
| `attributes.latestPaidDate` | object |  |
| `attributes.latestStageTransitionedAt` | string |  |
| `attributes.leadDeadAt` | object |  |
| `attributes.leadOpenedAt` | string |  |
| `attributes.leadPendingAt` | string |  |
| `attributes.leadQuotedAt` | object |  |
| `attributes.leadSoldAt` | object |  |
| `attributes.leadTypeId` | object |  |
| `attributes.materialTotal` | number |  |
| `attributes.name` | string |  |
| `attributes.nameNumber` | object |  |
| `attributes.namePrefix` | object |  |
| `attributes.openedAt` | object |  |
| `attributes.opportunityType` | string |  |
| `attributes.options.importBatchId` | number |  |
| `attributes.options.originalContractAmount` | number |  |
| `attributes.price` | number |  |
| `attributes.profileId` | object |  |
| `attributes.projectedCloseDate` | object |  |
| `attributes.propertyId` | number |  |
| `attributes.propertyName` | string |  |
| `attributes.recentActivity` | string |  |
| `attributes.scheduledAt` | object |  |
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

Through the native Centerpoint API, this operation is `GET productions/:PRODUCTION_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-production.md) for the provider-specific parameters and requirements.

