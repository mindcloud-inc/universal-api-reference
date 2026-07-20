# WorkflowMax: Create Job



```
POST https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "budget": 1,
      "capacityReducing": true,
      "client": {
        "email": "ava@example.com",
        "name": "Ava Chen",
        "phoneNumber": "string",
        "uuid": "string"
      },
      "clientManager": {
        "firstName": "Ava",
        "lastName": "Chen",
        "uuid": "string"
      },
      "clientOrderNumber": "string",
      "completedDate": "string",
      "contact": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "mobileNumber": "string",
        "phoneNumber": "string",
        "uuid": "string"
      },
      "createdAt": "string",
      "customFields": [
        {
          "name": "Ava Chen",
          "uuid": "string",
          "value": "string"
        }
      ],
      "description": "string",
      "dueDate": "string",
      "estimatedBillings": 1,
      "excludeEstimatedBillings": true,
      "jobCategory": {
        "jobCategory": "string",
        "uuid": "string"
      },
      "jobManager": {
        "firstName": "Ava",
        "lastName": "Chen",
        "uuid": "string"
      },
      "jobNumber": "string",
      "jobStatus": {
        "jobStatus": "string",
        "uuid": "string"
      },
      "name": "Ava Chen",
      "priority": "string",
      "staffAssigned": [
        {
          "customBillableRate": 1,
          "firstName": "Ava",
          "lastName": "Chen",
          "uuid": "string"
        }
      ],
      "startDate": "string",
      "taskInvoiceRate": "string",
      "updatedAt": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `budget` | number | The budget of the job. |
| `capacityReducing` | boolean | Indicate whether the job is capacity-reducing. It is setup in capacity planning. |
| `client.email` | string | The email address of the client associated with the job. |
| `client.name` | string | The name of the client associated with the job. |
| `client.phoneNumber` | string | The phone number of the client associated with the job. |
| `client.uuid` | string | The unique identifier of the client associated with the job. |
| `clientManager.firstName` | string | The first name of the client manager assigned to the job. |
| `clientManager.lastName` | string | The last name of the client manager assigned to the job. |
| `clientManager.uuid` | string | The unique identifier of the client manager assigned to the job. |
| `clientOrderNumber` | string | The client order number of the job. |
| `completedDate` | string | The date when the job was marked as completed. |
| `contact.email` | string | The email address of the contact associated with the job. |
| `contact.firstName` | string | The first name of the contact associated with the job. |
| `contact.lastName` | string | The last name of the contact associated with the job. |
| `contact.mobileNumber` | string | The mobile number of the contact associated with the job. |
| `contact.phoneNumber` | string | The phone number of the contact associated with the job. |
| `contact.uuid` | string | The unique identifier of the contact associated with the job. |
| `createdAt` | string | The UTC timestamp indicating when the job was created. |
| `customFields[].name` | string | The name of the custom field. |
| `customFields[].uuid` | string | The unique identifier of the custom field. |
| `customFields[].value` | string | The value of the custom field. |
| `description` | string | The description of the job. |
| `dueDate` | string | The date by which the job is expected to be completed. |
| `estimatedBillings` | number | The estimated billings amount of the job. |
| `excludeEstimatedBillings` | boolean | Indicate whether the job is excluded from estimated billings. |
| `jobCategory.jobCategory` | string | The name of the job category. |
| `jobCategory.uuid` | string | The unique identifier of the job category. |
| `jobManager.firstName` | string | The first name of the job manager assigned to the job. |
| `jobManager.lastName` | string | The last name of the job manager assigned to the job. |
| `jobManager.uuid` | string | The unique identifier of the job manager assigned to the job. |
| `jobNumber` | string | The internal or system-generated number assigned to identify the job. |
| `jobStatus.jobStatus` | string | The name of the job status. |
| `jobStatus.uuid` | string | The unique identifier of the job status. |
| `name` | string | The official title or designation of the job. |
| `priority` | string | The priority of the job. |
| `staffAssigned[].customBillableRate` | number | The custom billable rate of the staff who is assigned to the job. |
| `staffAssigned[].firstName` | string | The first name of the staff who is assigned to the job. |
| `staffAssigned[].lastName` | string | The last name of the staff who is assigned to the job. |
| `staffAssigned[].uuid` | string | The unique identifier of the staff who is assigned to the job. |
| `startDate` | string | The date when work on the job officially began. |
| `taskInvoiceRate` | string | The task invoice rate mode to be used in the job. Possible value: staff, task. |
| `updatedAt` | string | The UTC timestamp indicating when the job was last updated. |
| `uuid` | string | The unique identifier of the created job, returned in the response. |

## Native endpoint

Through the native WorkflowMax API, this operation is `POST v2/jobs` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

