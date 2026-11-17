# ECI Bolt: Get Work Order



```
GET https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/get-work-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/get-work-order?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/get-work-order?${params}`, {
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
| `id` | number | yes | Id of the work order. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointmentEndTime` | string |  |
| `appointmentStartTime` | string |  |
| `completedDate` | string |  |
| `createdAt` | string |  |
| `crewIds` | array<number> |  |
| `crewNtoes` | string |  |
| `crewPayExtraAddedPay` | number |  |
| `crews` | array |  |
| `departmentType` | string |  |
| `estimatedCompletionDate` | string |  |
| `etag` | string |  |
| `floorplanContractCharge` | number |  |
| `floorplanLaborCharge` | number |  |
| `floorplanOptionsCharges` | array |  |
| `homeOwner` | string |  |
| `homeOwnerEmail` | string |  |
| `homeOwnerPhone` | string |  |
| `id` | number |  |
| `jobExtrasCharges` | array |  |
| `jobNumber` | number |  |
| `laborTotal` | number |  |
| `notes` | string |  |
| `percentageOfCompletion` | number |  |
| `priceTotal` | number |  |
| `rescheduleDate` | string |  |
| `scheduleChangeComment` | string |  |
| `scheduleChangeReason` | string |  |
| `stage` | string |  |
| `supervisorId` | number |  |
| `updatedAt` | string |  |
| `warrantyIssue` | string |  |
| `warrantyIssueId` | number |  |
| `workOrderType` | string |  |
| `workOrderTypeId` | number |  |

## Native endpoint

Through the native ECI Bolt API, this operation is `GET /open/v1/work_orders/:id` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-work-order.md) for the provider-specific parameters and requirements.

