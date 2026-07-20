# WorkflowMax: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-invoices?${params}`, {
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
      "data": [
        {
          "amountExTax": 1,
          "amountIncTax": 1,
          "amountPaid": 1,
          "clientUUID": "string",
          "contactUUID": "string",
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
              "createdByUUID": "string",
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
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].amountExTax` | number | The total amount of the invoice excluding taxes. |
| `data[].amountIncTax` | number | The total amount of the invoice including taxes. |
| `data[].amountPaid` | number | The total amount paid for the invoice. |
| `data[].clientUUID` | string | The unique identifier for the client associated with the invoice. |
| `data[].contactUUID` | string | The unique identifier for the contact associated with the invoice. |
| `data[].createdAt` | string | The UTC date and time when the invoice was created. |
| `data[].date` | string | The date of the invoice. |
| `data[].datePaid` | string | The date when the invoice was paid. |
| `data[].description` | string | The description or details related to the invoice. |
| `data[].dueDate` | string | The due date for the invoice payment. |
| `data[].fixedPrice` | boolean | Indicate whether the price of the invoice is based on a fixed price. It is in calculated price if value is false. |
| `data[].invoiceNumber` | string | The unique invoice number for the invoice. It is only populated when the invoice is not a draft. |
| `data[].jobs[].clientOrderNumber` | string | The client's order number of the job. |
| `data[].jobs[].costs[].additional` | boolean | Indicate whether the invoice cost is added directly in the invoice. |
| `data[].jobs[].costs[].amount` | number | The total price of the invoice cost. |
| `data[].jobs[].costs[].billable` | boolean | Indicate whether the invoice is billable. |
| `data[].jobs[].costs[].costCode` | string | The code associated with the cost on the invoice. |
| `data[].jobs[].costs[].costNote` | string | Any additional notes related to the cost on the invoice. |
| `data[].jobs[].costs[].costUUID` | string | The unique identifier of the cost as managed in organization settings. |
| `data[].jobs[].costs[].createdAt` | string | The date and time when the invoice cost was created. |
| `data[].jobs[].costs[].description` | string | A detailed description of the invoice cost. |
| `data[].jobs[].costs[].fixedPrice` | boolean | Indicates if the invoice cost price is based on a fixed price. It is based on calculated mode if value is false. |
| `data[].jobs[].costs[].invoicePhaseUUID` | string | The unique identifier for the invoice phase of the task. It can be mapped with the uuid in phases section in this endpoint. |
| `data[].jobs[].costs[].jobCostUUID` | string | The unique identifier for the job cost related to the invoice. |
| `data[].jobs[].costs[].name` | string | The name of the invoice cost. |
| `data[].jobs[].costs[].order` | number | The order of the invoice cost. |
| `data[].jobs[].costs[].quantity` | number | The quantity of the invoice cost. |
| `data[].jobs[].costs[].tax[].taxName` | string | The name of the tax applied to the invoice task. |
| `data[].jobs[].costs[].tax[].taxRate` | string | The tax rate applied to the invoice task. |
| `data[].jobs[].costs[].tax[].taxType` | string | The tax rate applied to the invoice task. |
| `data[].jobs[].costs[].type` | string | The type of the invoice cost, e.g. service or stock. |
| `data[].jobs[].costs[].unitCost` | number | The unit cost for of the invoice cost. |
| `data[].jobs[].costs[].unitPrice` | number | The unit price of the invoice price. |
| `data[].jobs[].costs[].updatedAt` | string | The date and time when the invoice cost was last updated. |
| `data[].jobs[].costs[].uuid` | string | The unique identifier for the invoice cost. |
| `data[].jobs[].description` | string | A brief description of the job. |
| `data[].jobs[].name` | string | The name of the job. |
| `data[].jobs[].number` | string | The unique number assigned to the job. |
| `data[].jobs[].phases[].description` | string | The description of the invoice phase. |
| `data[].jobs[].phases[].jobPhaseUUID` | string | The unique identifier of the associated job phase. |
| `data[].jobs[].phases[].name` | string | The name of the invoice phase. |
| `data[].jobs[].phases[].order` | number | The order of the phase in the invoice. |
| `data[].jobs[].phases[].uuid` | string | The unique identifier of the invoice phase. |
| `data[].jobs[].taskInvoiceMode` | string | The mode of invoicing for the job, e.g. task or staff. |
| `data[].jobs[].tasks[].additional` | boolean | Indicate whether the invoice task is added directly in the invoice. |
| `data[].jobs[].tasks[].amount` | number | The total price of the invoice task. |
| `data[].jobs[].tasks[].billable` | boolean | Indicate if the invoice task is billable. |
| `data[].jobs[].tasks[].billableRate` | number | The billable rate for the invoice task. It only returns when  Case 1: It is an actual invoice, the invoice task is added in the invoice directly and there is no staff allocation for it, OR  Case 2: It is an actual invoice, the invoice task is from job and the job invoice mode is on task, OR  Case 3: It is a quoted invoice and there is no staff allocation for it. |
| `data[].jobs[].tasks[].createdAt` | string | The date and time when the invoice task was created. |
| `data[].jobs[].tasks[].description` | string | A brief description of the invoice task. |
| `data[].jobs[].tasks[].fixedPrice` | boolean | Indicates if the invoice task price is based on a fixed price. It is based on calculated mode if value is false. |
| `data[].jobs[].tasks[].invoicePhaseUUID` | string | The unique identifier for the invoice phase of the task. It can be mapped with the uuid in phases section in this endpoint. |
| `data[].jobs[].tasks[].jobTaskUUID` | string | The unique identifier for the job task related to the invoice. |
| `data[].jobs[].tasks[].label` | string | The label of the invoice task. |
| `data[].jobs[].tasks[].name` | string | The name of the invoice task. |
| `data[].jobs[].tasks[].order` | number | The order of the invoice task. |
| `data[].jobs[].tasks[].taskUUID` | string | The unique identifier of the task as managed in organization settings. |
| `data[].jobs[].tasks[].tax[].taxName` | string | The name of the tax applied to the invoice task. |
| `data[].jobs[].tasks[].tax[].taxRate` | string | The tax rate applied to the invoice task. |
| `data[].jobs[].tasks[].tax[].taxType` | string | The tax rate applied to the invoice task. |
| `data[].jobs[].tasks[].time` | number | The total time in minutes of the invoice task. |
| `data[].jobs[].tasks[].updatedAt` | string | The date and time when the invoice task was last updated. |
| `data[].jobs[].tasks[].uuid` | string | The unique identifier for the invoice task. |
| `data[].jobs[].uuid` | string | The unique identifier for the job. |
| `data[].mode` | string | The mode of the invoice, e.g. actual or quoted. |
| `data[].notes[].createdAt` | string | The date and time when the invoice note was created. |
| `data[].notes[].createdByUUID` | string | The unique identifier of the user who created the invoice note. |
| `data[].notes[].date` | string | The date of the invoice note. |
| `data[].notes[].description` | string | A brief description of the invoice note. |
| `data[].notes[].phase` | string | The phase of the invoice note. |
| `data[].notes[].title` | string | The title of the invoice note. |
| `data[].notes[].updatedAt` | string | The date and time when the invoice note was last updated. |
| `data[].notes[].uuid` | string | The unique identifier of the invoice note. |
| `data[].payments[].accountName` | string | The name of the account associated with the payment. |
| `data[].payments[].accountUUID` | string | The unique identifier of the account associated with the payment. It can be mapped with the uuid in GET /accounts endpoint. |
| `data[].payments[].amount` | number | The amount of the payment. |
| `data[].payments[].date` | string | The date when the payment happened. |
| `data[].payments[].reference` | string | The reference information of the payment. |
| `data[].payments[].updatedAt` | string | The date and time when the payment was last updated. |
| `data[].progressDate` | string | The progress date of the invoice, only the WIP on or before the progress date will be retrieved when creating an invoice. |
| `data[].sent` | boolean | Indicates whether the invoice has been sent to client. |
| `data[].status` | string | The status of the invoice, e.g. draft, cancelled, approved. |
| `data[].type` | string | The type of the invoice, e.g. progress invoice or final invoice. |
| `data[].updatedAt` | string | The UTC date and time when the invoice information was last updated. |
| `data[].uuid` | string | The unique identifier for the invoice. |
| `total` | number | The total number of invoices returned. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/invoices` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

