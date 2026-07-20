# WorkflowMax: Get Job



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-job?connectionId=$CONNECTION_ID&jobIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-job?${params}`, {
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
| `jobIdentifier` | string | yes | The WorkflowMax job identifier. |

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
      "costs": [
        {
          "actual": true,
          "billable": true,
          "costCode": "string",
          "costUUID": "string",
          "createdAt": "string",
          "customFields": [
            {
              "name": "Ava Chen",
              "uuid": "string",
              "value": "string"
            }
          ],
          "date": "string",
          "name": "Ava Chen",
          "note": "string",
          "phaseUUID": "string",
          "quantity": 1,
          "supplier": {
            "name": "Ava Chen",
            "uuid": "string"
          },
          "type": "string",
          "unitCost": 1,
          "unitPrice": 1,
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "createdAt": "string",
      "customFields": [
        {
          "name": "Ava Chen",
          "uuid": "string",
          "value": "string"
        }
      ],
      "deletedAt": "string",
      "description": "string",
      "documents": [
        {
          "createdAt": "string",
          "downloadURL": "https://example.com",
          "fileName": "Ava Chen",
          "fileSize": 1,
          "note": "string",
          "phaseUUID": "string",
          "title": "string",
          "updatedAt": "string",
          "uploadedBy": {
            "firstName": "Ava",
            "lastName": "Chen",
            "uuid": "string"
          },
          "uuid": "string"
        }
      ],
      "dueDate": "string",
      "estimatedBillings": 1,
      "excludeEstimatedBillings": true,
      "invoices": [
        {
          "amountExTax": 1,
          "amountIncTax": 1,
          "amountPaid": 1,
          "clientOrderNumber": "string",
          "clientUUID": "string",
          "contactUUID": "string",
          "createdAt": "string",
          "date": "string",
          "datePaid": "string",
          "dueDate": "string",
          "number": "string",
          "status": "string",
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
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
      "milestones": [
        {
          "completedBy": {
            "firstName": "Ava",
            "lastName": "Chen",
            "uuid": "string"
          },
          "completedDate": "string",
          "date": "string",
          "name": "Ava Chen",
          "phaseUUID": "string"
        }
      ],
      "name": "Ava Chen",
      "notes": [
        {
          "comments": [
            {
              "comment": "string",
              "createdAt": "string",
              "createdBy": {
                "firstName": "Ava",
                "lastName": "Chen",
                "uuid": "string"
              },
              "updatedAt": "string"
            }
          ],
          "createdAt": "string",
          "createdBy": {
            "firstName": "Ava",
            "lastName": "Chen",
            "uuid": "string"
          },
          "date": "string",
          "description": "string",
          "phaseUUID": "string",
          "title": "string",
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "phases": [
        {
          "createdAt": "string",
          "description": "string",
          "name": "Ava Chen",
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "priority": "string",
      "purchaseOrders": [
        {
          "amountExTax": 1,
          "amountIncTax": 1,
          "billingStatus": "string",
          "createdAt": "string",
          "date": "string",
          "receivingStatus": "string",
          "status": "string",
          "supplier": {
            "name": "Ava Chen",
            "uuid": "string"
          },
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "quotes": [
        {
          "amountExTax": 1,
          "amountIncTax": 1,
          "budget": 1,
          "clientUUID": "string",
          "contactUUID": "string",
          "createdAt": "string",
          "customFields": [
            {
              "name": "Ava Chen",
              "uuid": "string",
              "value": "string"
            }
          ],
          "isMasterQuote": true,
          "name": "Ava Chen",
          "number": "string",
          "salesPersonUUID": {
            "firstName": "Ava",
            "lastName": "Chen",
            "UUID": "string"
          },
          "status": "string",
          "type": "string",
          "updatedAt": "string",
          "uuid": "string",
          "validFrom": "string",
          "validTo": "string"
        }
      ],
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
      "tasks": [
        {
          "actualMinutes": 1,
          "billable": true,
          "completed": true,
          "createdAt": "string",
          "customBillableRate": 1,
          "customFields": [
            {
              "name": "Ava Chen",
              "uuid": "string",
              "value": "string"
            }
          ],
          "description": "string",
          "dueDate": "string",
          "estimatedMinutes": 1,
          "label": "string",
          "name": "Ava Chen",
          "phaseUUID": "string",
          "staffs": [
            {
              "allocatedTime": 1,
              "firstName": "Ava",
              "lastName": "Chen",
              "uuid": "string"
            }
          ],
          "startDate": "string",
          "taskUUID": "string",
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "timesheets": [
        {
          "billable": true,
          "createdAt": "string",
          "customFields": [
            {
              "name": "Ava Chen",
              "uuid": "string",
              "value": "string"
            }
          ],
          "date": "string",
          "finishTime": "string",
          "jobTaskUUID": "string",
          "minutes": 1,
          "note": "string",
          "staff": {
            "firstName": "Ava",
            "lastName": "Chen",
            "uuid": "string"
          },
          "startTime": "string",
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
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
| `budget` | number | The budget amount of the job. |
| `capacityReducing` | boolean | Indicate whether the job is capacity reducing. |
| `client.email` | string | The email address of the associated client. |
| `client.name` | string | The name of the associated client. |
| `client.phoneNumber` | string | The phone number of the associated client. |
| `client.uuid` | string | The unique identifier of the associated client. |
| `clientManager.firstName` | string | The first name of the job's client manager. |
| `clientManager.lastName` | string | The last name of the job's client manager. |
| `clientManager.uuid` | string | The unique identifier of the job's client manager. |
| `clientOrderNumber` | string | The client order number of the job. |
| `completedDate` | string | The completed date of the job. |
| `contact.email` | string | The email address of the associated client contact. |
| `contact.firstName` | string | The first name of the associated client contact. |
| `contact.lastName` | string | The last name of the associated client contact. |
| `contact.mobileNumber` | string | The mobile number of the associated client contact. |
| `contact.phoneNumber` | string | The phone number of the associated client contact. |
| `contact.uuid` | string | The unique identifier of the associated client contact. |
| `costs[].actual` | boolean | Indicate whether the job cost is an actual cost. It is an estimate cost if value is false. |
| `costs[].billable` | boolean | Indicate whether the job cost is billable. |
| `costs[].costCode` | string | The cost code of the job cost. |
| `costs[].costUUID` | string | The unique identifier of the cost. |
| `costs[].createdAt` | string | The UTC date and time when the job cost was created. |
| `costs[].customFields[].name` | string | The name of the job cost custom field. |
| `costs[].customFields[].uuid` | string | The unique identifier of the job cost custom field. |
| `costs[].customFields[].value` | string | The value of the job cost custom field. |
| `costs[].date` | string | The date of the job cost. |
| `costs[].name` | string | The name of the job cost. |
| `costs[].note` | string | The note of the job cost. |
| `costs[].phaseUUID` | string | The unique identifier of the job cost's phase. It can be mapped with the UUID in phases section. |
| `costs[].quantity` | number | The quantity of the job cost. |
| `costs[].supplier.name` | string | The name of the job cost's supplier. |
| `costs[].supplier.uuid` | string | The unique identifier of the job cost's supplier. |
| `costs[].type` | string | The type of the job cost (service or stock). |
| `costs[].unitCost` | number | The unit cost of the job cost. |
| `costs[].unitPrice` | number | The unit price of the job cost. |
| `costs[].updatedAt` | string | The UTC date and time when the job cost was last updated. |
| `costs[].uuid` | string | The unique identifier of the job cost. |
| `createdAt` | string | The UTC date and time when the job was created. |
| `customFields[].name` | string | The name of the job custom field. |
| `customFields[].uuid` | string | The unique identifier of the job custom field. |
| `customFields[].value` | string | The value of the job custom field. |
| `deletedAt` | string | The UTC date and time when the job was deleted. |
| `description` | string | The description of the job. |
| `documents[].createdAt` | string | The UTC date and time when the job document was created. |
| `documents[].downloadURL` | string | The download URL of the job document. |
| `documents[].fileName` | string | The file name of the job document. |
| `documents[].fileSize` | number | The file size of the job document. |
| `documents[].note` | string | The note of the job document. |
| `documents[].phaseUUID` | string | The unique identifier of the phase for the job document. It can be mapped with the UUID in phases section. |
| `documents[].title` | string | The title of the job document. |
| `documents[].updatedAt` | string | The UTC date and time when the job document was last updated. |
| `documents[].uploadedBy.firstName` | string | The first name of the staff who uploaded the job document. |
| `documents[].uploadedBy.lastName` | string | The last name of the staff who uploaded the job document. |
| `documents[].uploadedBy.uuid` | string | The unique identifier of the staff who uploaded the job document. |
| `documents[].uuid` | string | The unique identifier of the job document. |
| `dueDate` | string | The due date of the job. |
| `estimatedBillings` | number | The cached estimated billings amount of the job. |
| `excludeEstimatedBillings` | boolean | Indicate whether the job is excluded from estimated billings. |
| `invoices[].amountExTax` | number | The invoice amount excluding tax. |
| `invoices[].amountIncTax` | number | The invoice amount including tax. |
| `invoices[].amountPaid` | number | The amount already paid for the invoice. |
| `invoices[].clientOrderNumber` | string | The client order number of the invoice. |
| `invoices[].clientUUID` | string | The unique identifier of the client associated with the invoice. |
| `invoices[].contactUUID` | string | The unique identifier of the client contact associated with the invoice. |
| `invoices[].createdAt` | string | The UTC date and time when the invoice was created. |
| `invoices[].date` | string | The date of the invoice. |
| `invoices[].datePaid` | string | The date when the invoice is paid. |
| `invoices[].dueDate` | string | The due date of the invoice. |
| `invoices[].number` | string | The number of the invoice. |
| `invoices[].status` | string | The status of the invoice, returns draft, approved. |
| `invoices[].updatedAt` | string | The UTC date and time when the invoice was last updated. |
| `invoices[].uuid` | string | The unique identifier of the invoice. |
| `jobCategory.jobCategory` | string | The job category of the job. |
| `jobCategory.uuid` | string | The unique identifier of the job category maintained in job settings. |
| `jobManager.firstName` | string | The first name of the job's job manager. |
| `jobManager.lastName` | string | The last name of the job's job manager. |
| `jobManager.uuid` | string | The unique identifier of the job's job manager. |
| `jobNumber` | string | The number of the job. |
| `jobStatus.jobStatus` | string | The job status of the job. |
| `jobStatus.uuid` | string | The unique identifier of the job status maintained in job settings. |
| `milestones[].completedBy.firstName` | string | The first name of the staff who completed the milestone. |
| `milestones[].completedBy.lastName` | string | The last name of the staff who completed the milestone. |
| `milestones[].completedBy.uuid` | string | The unique identifier of the staff who completed the milestone. |
| `milestones[].completedDate` | string | Indicate whether the milestone is completed. |
| `milestones[].date` | string | The date of milestone. |
| `milestones[].name` | string | The name of the milestone. |
| `milestones[].phaseUUID` | string | The unique identifier of the milestone's phase. It can be mapped with the UUID in phases section. |
| `name` | string | The name of the job. |
| `notes[].comments[].comment` | string | The details of the comment for the note. |
| `notes[].comments[].createdAt` | string | The created timestamp of the comment for the note. |
| `notes[].comments[].createdBy.firstName` | string | The first name of the staff who created the comment for the note. |
| `notes[].comments[].createdBy.lastName` | string | The last name of the staff who created the comment for the note. |
| `notes[].comments[].createdBy.uuid` | string | The unique identifier of the staff who created the comment for the note. |
| `notes[].comments[].updatedAt` | string | The last updated timestamp of the comment for the note. |
| `notes[].createdAt` | string | The UTC date and time when the job note was created. |
| `notes[].createdBy.firstName` | string | The first name of the staff who created the job note. |
| `notes[].createdBy.lastName` | string | The last name of the staff who created the job note. |
| `notes[].createdBy.uuid` | string | The unique identifier of the staff who created the job note. |
| `notes[].date` | string | The date of the job note. |
| `notes[].description` | string | The description of the job note. |
| `notes[].phaseUUID` | string | The unique identifier of the job note's phase. It can be mapped with the UUID in phases section. |
| `notes[].title` | string | The title of the job note. |
| `notes[].updatedAt` | string | The UTC date and time when the job note was last updated. |
| `notes[].uuid` | string | The unique identifier of the job note. |
| `phases[].createdAt` | string | The UTC date and time when the job phase was created. |
| `phases[].description` | string | The description of the job phase. |
| `phases[].name` | string | The name of the job phase. |
| `phases[].updatedAt` | string | The UTC date and time when the job phase was last updated. |
| `phases[].uuid` | string | The unique identifier of the job phase. |
| `priority` | string | The priority of the job, returns Low, Normal, High, Immediate. |
| `purchaseOrders[].amountExTax` | number | The amount of the purchase order excluding tax. |
| `purchaseOrders[].amountIncTax` | number | The amount of the purchase order including tax. |
| `purchaseOrders[].billingStatus` | string | The billing status of the purchase order, returns awaiting, partial, full |
| `purchaseOrders[].createdAt` | string | The UTC date and time when the purchase order was created. |
| `purchaseOrders[].date` | string | The date of the purchase order. |
| `purchaseOrders[].receivingStatus` | string | The receiving status of the purchase order, returns awaiting, partial, full |
| `purchaseOrders[].status` | string | The general status of the purchase order, returns draft, issued, cancelled |
| `purchaseOrders[].supplier.name` | string | The name of the supplier associated with the purchase order. |
| `purchaseOrders[].supplier.uuid` | string | The unique identifier of the supplier associated with the purchase order. |
| `purchaseOrders[].updatedAt` | string | The UTC date and time when the purchase order was last updated. |
| `purchaseOrders[].uuid` | string | The unique identifier of the purchase order. |
| `quotes[].amountExTax` | number | The amount excluding tax for the quote. |
| `quotes[].amountIncTax` | number | The amount including tax for the quote. |
| `quotes[].budget` | number | The budget of the quote. |
| `quotes[].clientUUID` | string | The unique identifier of the client associated with the quote. |
| `quotes[].contactUUID` | string | The unique identifier of the client contact associated with the quote. |
| `quotes[].createdAt` | string | The UTC date and time when the quote was created. |
| `quotes[].customFields[].name` | string | The name of the quote custom field. |
| `quotes[].customFields[].uuid` | string | The unique identifier of the quote custom field. |
| `quotes[].customFields[].value` | string | The value of the quote custom field. |
| `quotes[].isMasterQuote` | boolean | Indicate whether it is a master quote of the job. |
| `quotes[].name` | string | The name of the quote. |
| `quotes[].number` | string | The number of the quote. |
| `quotes[].salesPersonUUID.firstName` | string | The first name of the sales person for the quote. |
| `quotes[].salesPersonUUID.lastName` | string | The last name of the sales person for the quote. |
| `quotes[].salesPersonUUID.UUID` | string | The unique identifier of the sales person for the quote. |
| `quotes[].status` | string | The status of the quote, returns draft, issued, accepted, declined, revised |
| `quotes[].type` | string | The type of the quote, returns quote or estimate. |
| `quotes[].updatedAt` | string | The UTC date and time when the quote was last updated. |
| `quotes[].uuid` | string | The unique identifier of the quote. |
| `quotes[].validFrom` | string | The date from when the quote is valid. |
| `quotes[].validTo` | string | The date to when the quote is valid. |
| `staffAssigned[].customBillableRate` | number | The custom billable rate of the staff for the job. It is only valid when the task invoice mode is Staff. |
| `staffAssigned[].firstName` | string | The first name of the staff who is assigned to the job. |
| `staffAssigned[].lastName` | string | The last name of the staff who is assigned to the job. |
| `staffAssigned[].uuid` | string | The unique identifier of the staff who is assigned to the job. |
| `startDate` | string | The start date of the job. |
| `taskInvoiceRate` | string | The task invoice mode of the job, reflecting the job financial settings, returns staff or task. |
| `tasks[].actualMinutes` | number | The actual time in minutes of the job task. |
| `tasks[].billable` | boolean | Indicate whether the job task is billable. |
| `tasks[].completed` | boolean | Indicate whether the job task has been completed. |
| `tasks[].createdAt` | string | The UTC date and time when the job task was created. |
| `tasks[].customBillableRate` | number | The custom billable rate of the task for the job. It is only valid when the task invoice mode is Task. |
| `tasks[].customFields[].name` | string | The name of the job task custom field. |
| `tasks[].customFields[].uuid` | string | The unique identifier of the job task custom field. |
| `tasks[].customFields[].value` | string | The value of the job task custom field. |
| `tasks[].description` | string | The description of the job task. |
| `tasks[].dueDate` | string | The due date of the job task. |
| `tasks[].estimatedMinutes` | number | The estimated time in minutes of the job task. |
| `tasks[].label` | string | The label of the job task. |
| `tasks[].name` | string | The name of the job task. |
| `tasks[].phaseUUID` | string | The unique identifier of the job task's phase. It can be mapped with the UUID in phases section. |
| `tasks[].staffs[].allocatedTime` | number | The allocated time of the staff to the job task. |
| `tasks[].staffs[].firstName` | string | The first name of the staff allocated to the job task. |
| `tasks[].staffs[].lastName` | string | The last name of the staff allocated to the job task. |
| `tasks[].staffs[].uuid` | string | The unique identifier of the staff allocated to the job task. |
| `tasks[].startDate` | string | The start date of the job task. |
| `tasks[].taskUUID` | string | The unique identifier of the task. |
| `tasks[].updatedAt` | string | The UTC date and time when the job task was last updated. |
| `tasks[].uuid` | string | The unique identifier of the job task. |
| `timesheets[].billable` | boolean | Indicate whether the timesheet entry is billable. |
| `timesheets[].createdAt` | string | The UTC date and time when the job timesheet was created. |
| `timesheets[].customFields[].name` | string | The name for the timesheet entry's custom field. |
| `timesheets[].customFields[].uuid` | string | The unique identifier for the timesheet entry's custom field. |
| `timesheets[].customFields[].value` | string | The value for the timesheet entry's custom field. |
| `timesheets[].date` | string | The date of the timesheet entry. |
| `timesheets[].finishTime` | string | The finish time of the timesheet entry. It only returns when there is value for it. |
| `timesheets[].jobTaskUUID` | string | The unique identifier of the job task associated with the time entry. |
| `timesheets[].minutes` | number | The time in minutes logged for the timesheet entry. |
| `timesheets[].note` | string | The note of the timesheet entry. |
| `timesheets[].staff.firstName` | string | The first name of the staff for the timesheet entry. |
| `timesheets[].staff.lastName` | string | The last name of the staff for the timesheet entry. |
| `timesheets[].staff.uuid` | string | The unique identifier of the staff for the timesheet entry. |
| `timesheets[].startTime` | string | The start time of the timesheet entry. It only returns when there is value for it. |
| `timesheets[].updatedAt` | string | The UTC date and time when the job timesheet was last updated. |
| `timesheets[].uuid` | string | The unique identifier of the time entry. |
| `updatedAt` | string | The UTC date and time when the job was last updated. |
| `uuid` | string | The unique identifier for the job. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/jobs/{identifier}` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

