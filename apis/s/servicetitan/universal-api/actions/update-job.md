# ServiceTitan: Update Job

Updates an existing job in ServiceTitan.

```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | number | yes | The ServiceTitan job ID to update. |
| `customerId` | number | no | ID of the job's customer. |
| `locationId` | number | no | ID of the job's location. |
| `businessUnitId` | number | no | ID of the job's business unit. |
| `jobTypeId` | number | no | ID of the job type. |
| `priority` | string | no | Job priority value accepted by ServiceTitan. |
| `campaignId` | number | no | ID of the campaign associated with the job. |
| `summary` | string | no | Job summary. ServiceTitan accepts HTML. |
| `customerPo` | string | no | Customer purchase order value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobGeneratedLeadSource` | object<object> | no | Optional generated lead source object containing a job ID and/or employee ID. |
| `jobGeneratedLeadSource.jobId` | number | no | ID of the job from which this job was generated. |
| `jobGeneratedLeadSource.employeeId` | number | no | ID of the office user or technician that generated the lead. |
| `shouldUpdateInvoiceItems` | boolean | no | When true, also updates the business unit on invoice items for the job. |
| `customFields[]` | array<object> | no | Complete custom-field array. Sending this field replaces all existing custom-field values on the job. |
| `customFields[].typeId` | number | no | ID of the custom field. |
| `customFields[].value` | string | no | Value of the custom field. |
| `tagTypeIds[]` | array<number> | no | Complete tag type ID array. Sending this field replaces all existing tags on the job. |
| `externalData` | object<object> | no | External data update object. applicationGuid and externalData entries are required when this object is provided. |
| `externalData.patchMode` | list | no | Replace removes omitted keys; Merge changes only supplied keys. One of: `Merge`, `Replace`. |
| `externalData.applicationGuid` | string | no | Application GUID that owns the external data. |
| `externalData.externalDataList[]` | array<object> | no | External data entries containing key and value. |
| `externalData.externalDataList[].key` | string | no | External data key. |
| `externalData.externalDataList[].value` | string | no | External data value. A null value deletes the key when using Merge. |
| `soldById` | number | no | ID of the technician credited with selling the job. |
| `isAutoDispatched` | boolean | no | Whether Dispatch Pro is enabled for this job. |
| `summaryOfWork` | string | no | Summary of completed work. This ServiceTitan field is available only to enabled accounts. |
| `noCharge` | boolean | no | Whether the job is a no-charge job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointmentCount": 1,
      "bookingId": 1,
      "businessUnitId": 1,
      "campaignId": 1,
      "completedOn": "2026-05-07T12:00:00.000Z",
      "createdById": 1,
      "createdFromEstimateId": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "customerPo": "string",
      "customFields": [
        [
          {}
        ]
      ],
      "equipmentIds": [
        [
          1
        ]
      ],
      "estimateIds": [
        [
          1
        ]
      ],
      "externalData": [
        [
          {}
        ]
      ],
      "firstAppointmentId": 1,
      "id": 1,
      "invoiceId": 1,
      "isAutoDispatched": true,
      "jobGeneratedLeadSource": {
        "employeeId": 1,
        "jobId": 1
      },
      "jobNumber": "string",
      "jobStatus": "string",
      "jobTypeId": 1,
      "lastAppointmentId": 1,
      "leadCallId": 1,
      "locationId": 1,
      "membershipId": 1,
      "modifiedOn": "2026-05-07T12:00:00.000Z",
      "noCharge": true,
      "notificationsEnabled": true,
      "partnerLeadCallId": 1,
      "priority": "string",
      "projectId": 1,
      "recallForId": 1,
      "soldById": 1,
      "summary": "string",
      "summaryOfWork": "string",
      "tagTypeIds": [
        [
          1
        ]
      ],
      "total": 1,
      "warrantyId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointmentCount` | number |  |
| `bookingId` | number |  |
| `businessUnitId` | number |  |
| `campaignId` | number |  |
| `completedOn` | date |  |
| `createdById` | number |  |
| `createdFromEstimateId` | number |  |
| `createdOn` | date |  |
| `customerId` | number |  |
| `customerPo` | string |  |
| `customFields[]` | array<object> |  |
| `customFields[].name` | string |  |
| `customFields[].typeId` | number |  |
| `customFields[].value` | string |  |
| `equipmentIds[]` | array<number> |  |
| `estimateIds[]` | array<number> |  |
| `externalData[]` | array<object> |  |
| `externalData[].key` | string |  |
| `externalData[].value` | string |  |
| `firstAppointmentId` | number |  |
| `id` | number | ServiceTitan job ID. |
| `invoiceId` | number |  |
| `isAutoDispatched` | boolean |  |
| `jobGeneratedLeadSource` | object |  |
| `jobGeneratedLeadSource.employeeId` | number |  |
| `jobGeneratedLeadSource.jobId` | number |  |
| `jobNumber` | string |  |
| `jobStatus` | string |  |
| `jobTypeId` | number |  |
| `lastAppointmentId` | number |  |
| `leadCallId` | number |  |
| `locationId` | number |  |
| `membershipId` | number |  |
| `modifiedOn` | date |  |
| `noCharge` | boolean |  |
| `notificationsEnabled` | boolean |  |
| `partnerLeadCallId` | number |  |
| `priority` | string |  |
| `projectId` | number |  |
| `recallForId` | number |  |
| `soldById` | number |  |
| `summary` | string |  |
| `summaryOfWork` | string |  |
| `tagTypeIds[]` | array<number> |  |
| `total` | number |  |
| `warrantyId` | number |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `PATCH jpm/v2/tenant/{{credentials.tenant}}/jobs/:jobId` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job.md) for the provider-specific parameters and requirements.

