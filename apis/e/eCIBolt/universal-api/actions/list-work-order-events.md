# ECI Bolt: List Work Order Events



```
GET https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-work-order-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-work-order-events?connectionId=$CONNECTION_ID&eventToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-work-order-events?${params}`, {
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
| `eventToken` | string | yes | Token used to get the next list of events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {
          "author": "string",
          "authorId": 1,
          "changes": {},
          "createdAt": "string",
          "event": "string",
          "workOrder": {
            "appointmentEndTime": "string",
            "appointmentStartTime": "string",
            "completedDate": "string",
            "createdAt": "string",
            "crewIds": [
              1
            ],
            "crewNtoes": "string",
            "crewPayExtraAddedPay": 1,
            "crews": [
              "string"
            ],
            "departmentType": "string",
            "estimatedCompletionDate": "string",
            "etag": "string",
            "floorplanContractCharge": 1,
            "floorplanLaborCharge": 1,
            "floorplanOptionsCharges": [
              "string"
            ],
            "homeOwner": "string",
            "homeOwnerEmail": "ava@example.com",
            "homeOwnerPhone": "string",
            "id": 1,
            "jobExtrasCharges": [
              "string"
            ],
            "jobNumber": 1,
            "laborTotal": 1,
            "notes": "string",
            "percentageOfCompletion": 1,
            "priceTotal": 1,
            "rescheduleDate": "string",
            "scheduleChangeComment": "string",
            "scheduleChangeReason": "string",
            "stage": "string",
            "supervisorId": 1,
            "updatedAt": "string",
            "warrantyIssue": "string",
            "warrantyIssueId": 1,
            "workOrderType": "string",
            "workOrderTypeId": 1
          }
        }
      ],
      "eventToken": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> |  |
| `events[].author` | string |  |
| `events[].authorId` | number |  |
| `events[].changes` | object |  |
| `events[].createdAt` | string |  |
| `events[].event` | string |  |
| `events[].workOrder` | object |  |
| `events[].workOrder.appointmentEndTime` | string |  |
| `events[].workOrder.appointmentStartTime` | string |  |
| `events[].workOrder.completedDate` | string |  |
| `events[].workOrder.createdAt` | string |  |
| `events[].workOrder.crewIds` | array<number> |  |
| `events[].workOrder.crewNtoes` | string |  |
| `events[].workOrder.crewPayExtraAddedPay` | number |  |
| `events[].workOrder.crews` | array |  |
| `events[].workOrder.departmentType` | string |  |
| `events[].workOrder.estimatedCompletionDate` | string |  |
| `events[].workOrder.etag` | string |  |
| `events[].workOrder.floorplanContractCharge` | number |  |
| `events[].workOrder.floorplanLaborCharge` | number |  |
| `events[].workOrder.floorplanOptionsCharges` | array |  |
| `events[].workOrder.homeOwner` | string |  |
| `events[].workOrder.homeOwnerEmail` | string |  |
| `events[].workOrder.homeOwnerPhone` | string |  |
| `events[].workOrder.id` | number |  |
| `events[].workOrder.jobExtrasCharges` | array |  |
| `events[].workOrder.jobNumber` | number |  |
| `events[].workOrder.laborTotal` | number |  |
| `events[].workOrder.notes` | string |  |
| `events[].workOrder.percentageOfCompletion` | number |  |
| `events[].workOrder.priceTotal` | number |  |
| `events[].workOrder.rescheduleDate` | string |  |
| `events[].workOrder.scheduleChangeComment` | string |  |
| `events[].workOrder.scheduleChangeReason` | string |  |
| `events[].workOrder.stage` | string |  |
| `events[].workOrder.supervisorId` | number |  |
| `events[].workOrder.updatedAt` | string |  |
| `events[].workOrder.warrantyIssue` | string |  |
| `events[].workOrder.warrantyIssueId` | number |  |
| `events[].workOrder.workOrderType` | string |  |
| `events[].workOrder.workOrderTypeId` | number |  |
| `eventToken` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ECI Bolt API, this operation is `GET /open/v1/work_orders/events` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-work-order-events.md) for the provider-specific parameters and requirements.

