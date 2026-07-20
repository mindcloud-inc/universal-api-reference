# WorkflowMax: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | string | yes | The WorkflowMax invoice UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountExTax": 1,
      "amountIncTax": 1,
      "amountPaid": 1,
      "client": {
        "email": "ava@example.com",
        "name": "Ava Chen",
        "phoneNumber": "string",
        "uuid": "string"
      },
      "contact": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "mobileNumber": "string",
        "phoneNumber": "string",
        "uuid": "string"
      },
      "createdAt": "string",
      "date": "string",
      "datePaid": "string",
      "description": "string",
      "dueDate": "string",
      "fixedPrice": true,
      "invoiceNumber": "string",
      "jobs": [
        {
          "clientOrderNumber": "string",
          "costs": [
            {
              "additional": true,
              "amount": 1,
              "billable": true,
              "costCode": "string",
              "costNote": "string",
              "costUUID": "string",
              "createdAt": "string",
              "description": "string",
              "fixedPrice": true,
              "invoicePhaseUUID": "string",
              "jobCostUUID": "string",
              "name": "Ava Chen",
              "order": 1,
              "quantity": 1,
              "tax": [
                {
                  "taxName": "Ava Chen",
                  "taxRate": "string",
                  "taxType": "string"
                }
              ],
              "type": "string",
              "unitCost": 1,
              "unitPrice": 1,
              "updatedAt": "string",
              "uuid": "string"
            }
          ],
          "description": "string",
          "name": "Ava Chen",
          "number": "string",
          "phases": [
            {
              "description": "string",
              "jobPhaseUUID": "string",
              "name": "Ava Chen",
              "order": 1,
              "uuid": "string"
            }
          ],
          "taskInvoiceMode": "string",
          "tasks": [
            {
              "additional": true,
              "amount": 1,
              "billable": true,
              "billableRate": 1,
              "createdAt": "string",
              "description": "string",
              "fixedPrice": true,
              "invoicePhaseUUID": "string",
              "jobTaskUUID": "string",
              "label": "string",
              "name": "Ava Chen",
              "order": 1,
              "taskUUID": "string",
              "tax": [
                {
                  "taxName": "Ava Chen",
                  "taxRate": "string",
                  "taxType": "string"
                }
              ],
              "time": 1,
              "timeBreakDown": [
                {
                  "billableRate": 1,
                  "date": "string",
                  "invoiceBillable": "string",
                  "invoiceTimesheetUUID": "string",
                  "jobTimesheetUUID": "string",
                  "staffFirstName": "Ava",
                  "staffLastName": "Chen",
                  "staffUUID": "string",
                  "time": 1
                }
              ],
              "updatedAt": "string",
              "uuid": "string"
            }
          ],
          "uuid": "string"
        }
      ],
      "mode": "string",
      "notes": [
        {
          "createdAt": "string",
          "createdBy": {
            "firstName": "Ava",
            "lastName": "Chen",
            "uuid": "string"
          },
          "date": "string",
          "description": "string",
          "phase": "string",
          "title": "string",
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "payments": [
        {
          "accountName": "Ava Chen",
          "accountUUID": "string",
          "amount": 1,
          "createdAt": "string",
          "date": "string",
          "reference": "string",
          "updatedAt": "string"
        }
      ],
      "progressDate": "string",
      "sent": true,
      "status": "string",
      "type": "string",
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
| `amountExTax` | number | The total amount of the invoice excluding taxes. |
| `amountIncTax` | number | The total amount of the invoice including taxes. |
| `amountPaid` | number | The total amount paid for the invoice. |
| `client.email` | string | The email address of the client associated with the invoice. |
| `client.name` | string | The name of the client associated with the invoice. |
| `client.phoneNumber` | string | The phone number of the client associated with the invoice. |
| `client.uuid` | string | The unique identifier for the client associated with the invoice. |
| `contact.email` | string | The email address of the contact associated with the invoice. |
| `contact.firstName` | string | The first name of the contact associated with the invoice. |
| `contact.lastName` | string | The last name of the contact associated with the invoice. |
| `contact.mobileNumber` | string | The mobile number of the contact associated with the invoice. |
| `contact.phoneNumber` | string | The phone number of the contact associated with the invoice. |
| `contact.uuid` | string | The unique identifier of the contact associated with the invoice. |
| `createdAt` | string | The UTC date and time when the invoice was created. |
| `date` | string | The date of the invoice. |
| `datePaid` | string | The date when the invoice was paid. |
| `description` | string | The description or details related to the invoice. |
| `dueDate` | string | The due date for the invoice payment. |
| `fixedPrice` | boolean | Indicate whether the price of the invoice is based on a fixed price. It is in calculated price if value is false. |
| `invoiceNumber` | string | The unique invoice number for the invoice. It is only populated when the invoice is not a draft. |
| `jobs[].clientOrderNumber` | string | The client's order number of the job. |
| `jobs[].costs[].additional` | boolean | Indicate whether the invoice cost is added directly in the invoice. |
| `jobs[].costs[].amount` | number | The total price of the invoice cost. |
| `jobs[].costs[].billable` | boolean | Indicate whether the invoice is billable. |
| `jobs[].costs[].costCode` | string | The code associated with the cost on the invoice. |
| `jobs[].costs[].costNote` | string | Any additional notes related to the cost on the invoice. |
| `jobs[].costs[].costUUID` | string | The unique identifier of the cost as managed in organization settings. |
| `jobs[].costs[].createdAt` | string | The UTC date and time when the invoice cost was created. |
| `jobs[].costs[].description` | string | A detailed description of the invoice cost. |
| `jobs[].costs[].fixedPrice` | boolean | Indicates if the invoice cost price is based on a fixed price. It is based on calculated mode if value is false. |
| `jobs[].costs[].invoicePhaseUUID` | string | The unique identifier for the invoice phase of the task. It can be mapped with the uuid in phases section in this endpoint. |
| `jobs[].costs[].jobCostUUID` | string | The unique identifier for the job cost related to the invoice. |
| `jobs[].costs[].name` | string | The name of the invoice cost. |
| `jobs[].costs[].order` | number | The order of the invoice cost. |
| `jobs[].costs[].quantity` | number | The quantity of the invoice cost. |
| `jobs[].costs[].tax[].taxName` | string | The name of the tax applied to the invoice task. |
| `jobs[].costs[].tax[].taxRate` | string | The tax rate applied to the invoice task. |
| `jobs[].costs[].tax[].taxType` | string | The tax rate applied to the invoice task. |
| `jobs[].costs[].type` | string | The type of the invoice cost, e.g. service or stock. |
| `jobs[].costs[].unitCost` | number | The unit cost for of the invoice cost. |
| `jobs[].costs[].unitPrice` | number | The unit price of the invoice price. |
| `jobs[].costs[].updatedAt` | string | The UTC date and time when the invoice cost was last updated. |
| `jobs[].costs[].uuid` | string | The unique identifier for the invoice cost. |
| `jobs[].description` | string | A brief description of the job. |
| `jobs[].name` | string | The name of the job. |
| `jobs[].number` | string | The unique number assigned to the job. |
| `jobs[].phases[].description` | string | The description of the invoice phase. |
| `jobs[].phases[].jobPhaseUUID` | string | The unique identifier of the associated job phase. |
| `jobs[].phases[].name` | string | The name of the invoice phase. |
| `jobs[].phases[].order` | number | The order of the phase in the invoice. |
| `jobs[].phases[].uuid` | string | The unique identifier of the invoice phase. |
| `jobs[].taskInvoiceMode` | string | The mode of invoicing for the job, e.g. task or staff. |
| `jobs[].tasks[].additional` | boolean | Indicate whether the invoice task is added directly in the invoice. |
| `jobs[].tasks[].amount` | number | The total price of the invoice task. |
| `jobs[].tasks[].billable` | boolean | Indicate if the invoice task is billable. |
| `jobs[].tasks[].billableRate` | number | The billable rate for the invoice task. It only returns when  Case 1: It is an actual invoice, the invoice task is added in the invoice directly and there is no staff allocation for it, OR  Case 2: It is an actual invoice, the invoice task is from job and the job invoice mode is on task, OR  Case 3: It is a quoted invoice and there is no staff allocation for it. |
| `jobs[].tasks[].createdAt` | string | The UTC date and time when the invoice task was created. |
| `jobs[].tasks[].description` | string | A brief description of the invoice task. |
| `jobs[].tasks[].fixedPrice` | boolean | Indicates if the invoice task price is based on a fixed price. It is based on calculated mode if value is false. |
| `jobs[].tasks[].invoicePhaseUUID` | string | The unique identifier for the invoice phase of the task. It can be mapped with the uuid in phases section in this endpoint. |
| `jobs[].tasks[].jobTaskUUID` | string | The unique identifier for the job task related to the invoice. |
| `jobs[].tasks[].label` | string | The label of the invoice task. |
| `jobs[].tasks[].name` | string | The name of the invoice task. |
| `jobs[].tasks[].order` | number | The order of the invoice task. |
| `jobs[].tasks[].taskUUID` | string | The unique identifier of the task as managed in organization settings. |
| `jobs[].tasks[].tax[].taxName` | string | The name of the tax applied to the invoice task. |
| `jobs[].tasks[].tax[].taxRate` | string | The tax rate applied to the invoice task. |
| `jobs[].tasks[].tax[].taxType` | string | The tax rate applied to the invoice task. |
| `jobs[].tasks[].time` | number | The total time in minutes of the invoice task. |
| `jobs[].tasks[].timeBreakDown[].billableRate` | number | Billable rate of the invoice timesheet. |
| `jobs[].tasks[].timeBreakDown[].date` | string | The date of the invoice timesheet. It only returns in Case 1. |
| `jobs[].tasks[].timeBreakDown[].invoiceBillable` | string | Indicate whether the timesheet is billable in the invoice, e.g. Yes, No, Future. It only returns in Case 1. |
| `jobs[].tasks[].timeBreakDown[].invoiceTimesheetUUID` | string | The unique identifier of the invoice timesheet. It only returns in Case 2 and Case 3. |
| `jobs[].tasks[].timeBreakDown[].jobTimesheetUUID` | string | The unique identifier of the job timesheet which is linked to the invoice timesheet. It only returns in Case 1. |
| `jobs[].tasks[].timeBreakDown[].staffFirstName` | string | The first name of the staff member related to the invoice timesheet. |
| `jobs[].tasks[].timeBreakDown[].staffLastName` | string | The last name of the staff member related to the invoice timesheet. |
| `jobs[].tasks[].timeBreakDown[].staffUUID` | string | The unique identifier of the staff member related to the invoice timesheet. |
| `jobs[].tasks[].timeBreakDown[].time` | number | Time in minutes of the invoice timesheet. |
| `jobs[].tasks[].updatedAt` | string | The UTC date and time when the invoice task was last updated. |
| `jobs[].tasks[].uuid` | string | The unique identifier for the invoice task. |
| `jobs[].uuid` | string | The unique identifier for the job. |
| `mode` | string | The mode of the invoice, e.g. actual or quoted. |
| `notes[].createdAt` | string | The UTC date and time when the invoice was created. |
| `notes[].createdBy.firstName` | string | The first name of the staff who created the invoice note. |
| `notes[].createdBy.lastName` | string | The last name of the staff who created the invoice note. |
| `notes[].createdBy.uuid` | string | The unique identifier of the staff who created the invoice note. |
| `notes[].date` | string | The UTC date of the invoice note. |
| `notes[].description` | string | A brief description of the invoice note. |
| `notes[].phase` | string | The phase of the invoice note. |
| `notes[].title` | string | The title of the invoice note. |
| `notes[].updatedAt` | string | The UTC date and time when the invoice was last updated. |
| `notes[].uuid` | string | The unique identifier of the invoice note. |
| `payments[].accountName` | string | The name of the account associated with the payment. |
| `payments[].accountUUID` | string | The unique identifier of the account associated with the payment. It can be mapped with the uuid in GET /accounts endpoint. |
| `payments[].amount` | number | The amount of the payment. |
| `payments[].createdAt` | string | The UTC date and time when the payment was last updated. |
| `payments[].date` | string | The date when the payment happened. |
| `payments[].reference` | string | The reference information of the payment. |
| `payments[].updatedAt` | string | The UTC date and time when the payment was last updated. |
| `progressDate` | string | The progress date of the invoice, only the WIP on or before the progress date will be retrieved when creating an invoice. |
| `sent` | boolean | Indicates whether the invoice has been sent to client. |
| `status` | string | The status of the invoice, e.g. draft, cancelled, approved. |
| `type` | string | The type of the invoice, e.g. progress invoice or final invoice. |
| `updatedAt` | string | The UTC date and time when the invoice information was last updated. |
| `uuid` | string | The unique identifier for the invoice. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/invoices/{UUID}` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

