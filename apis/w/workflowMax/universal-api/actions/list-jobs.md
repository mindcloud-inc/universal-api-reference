# WorkflowMax: List Jobs



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-jobs?${params}`, {
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
          "budget": 1,
          "capacityReducing": true,
          "clientContactUUID": "string",
          "clientManagerUUID": "string",
          "clientOrderNumber": "string",
          "clientUUID": "string",
          "completedDate": "string",
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
              "supplierUUID": "string",
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
              "uploadedByUUID": "string",
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
          "jobCategoryUUID": "string",
          "jobManagerUUID": "string",
          "jobNumber": "string",
          "jobStatusUUID": "string",
          "milestones": [
            {
              "completed": true,
              "date": "string",
              "name": "Ava Chen",
              "phaseUUID": "string"
            }
          ],
          "name": "Ava Chen",
          "notes": [
            {
              "createdAt": "string",
              "createdByUUID": "string",
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
              "supplierUUID": "string",
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
              "salesPersonUUID": "string",
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
              "staff": [
                {
                  "allocatedTime": 1,
                  "uuid": "string"
                }
              ],
              "startDate": "string",
              "taskUUID": "string",
              "updatedAt": "string",
              "uuid": "string"
            }
          ],
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
| `data[].budget` | number | The budget of the job. |
| `data[].capacityReducing` | boolean | Indicate whether the job is capacity reducing. |
| `data[].clientContactUUID` | string | The unique identifier of the associated client contact. |
| `data[].clientManagerUUID` | string | The unique identifier of the job's client manager. |
| `data[].clientOrderNumber` | string | The dlient order number of the job. |
| `data[].clientUUID` | string | The unique identifier of the associated client. |
| `data[].completedDate` | string | The completed date of the job. |
| `data[].costs[].actual` | boolean | Indicate whether the job cost is an actual cost. It is an estimate cost if value is false. |
| `data[].costs[].billable` | boolean | Indicate whether the job cost is billable. |
| `data[].costs[].costCode` | string | The cost code of the job cost. |
| `data[].costs[].costUUID` | string | The unique identifier of the cost. |
| `data[].costs[].createdAt` | string | The UTC date and time when the job cost was created. |
| `data[].costs[].customFields[].name` | string | The name of the job cost custom field. |
| `data[].costs[].customFields[].uuid` | string | The unique identifier of the job cost custom field. |
| `data[].costs[].customFields[].value` | string | The value of the job cost custom field. |
| `data[].costs[].date` | string | The date of the job cost. |
| `data[].costs[].name` | string | The name of the job cost. |
| `data[].costs[].note` | string | The note of the job cost. |
| `data[].costs[].phaseUUID` | string | The unique identifier of the job cost's phase. It can be mapped with the UUID in phases section. |
| `data[].costs[].quantity` | number | The quantity of the job cost. |
| `data[].costs[].supplierUUID` | string | The unique identifier of the job cost's supplier. |
| `data[].costs[].type` | string | The type of the job cost (service or stock). |
| `data[].costs[].unitCost` | number | The unit cost of the job cost. |
| `data[].costs[].unitPrice` | number | The unit price of the job cost. |
| `data[].costs[].updatedAt` | string | The UTC date and time when the job cost was created. |
| `data[].costs[].uuid` | string | The unique identifier of the job cost. |
| `data[].createdAt` | string | The UTC date and time when the job was created. |
| `data[].customFields[].name` | string | The name of the job custom field. |
| `data[].customFields[].uuid` | string | The unique identifier of the job custom field. |
| `data[].customFields[].value` | string | The value of the job custom field. |
| `data[].deletedAt` | string | The UTC date and time when the job was deleted. |
| `data[].description` | string | The description of the job. |
| `data[].documents[].createdAt` | string | The UTC date and time when the job document was created. |
| `data[].documents[].downloadURL` | string | The download URL of the job document. |
| `data[].documents[].fileName` | string | The file name of the job document. |
| `data[].documents[].fileSize` | number | The file size of the job document. |
| `data[].documents[].note` | string | The note of the job document. |
| `data[].documents[].phaseUUID` | string | The unique identifier of the phase for the job document. It can be mapped with the UUID in phases section. |
| `data[].documents[].title` | string | The title of the job document. |
| `data[].documents[].updatedAt` | string | The UTC date and time when the job document was last updated. |
| `data[].documents[].uploadedByUUID` | string | The unique identifier of the staff who uploaded the job document. |
| `data[].documents[].uuid` | string | The unique identifier of the job document. |
| `data[].dueDate` | string | The due date of the job. |
| `data[].estimatedBillings` | number | The cached estimated billings amount of the job. |
| `data[].excludeEstimatedBillings` | boolean | Indicate whether the job is excluded from estimated billings. |
| `data[].invoices[].amountExTax` | number | The invoice amount excluding tax. |
| `data[].invoices[].amountIncTax` | number | The invoice amount including tax. |
| `data[].invoices[].amountPaid` | number | The amount already paid for the invoice. |
| `data[].invoices[].clientOrderNumber` | string | The client order number of the invoice. |
| `data[].invoices[].clientUUID` | string | The unique identifier of the client associated with the invoice. |
| `data[].invoices[].contactUUID` | string | The unique identifier of the client contact associated with the invoice. |
| `data[].invoices[].createdAt` | string | The UTC date and time when the invoice was created. |
| `data[].invoices[].date` | string | The date of the invoice. |
| `data[].invoices[].datePaid` | string | The date when the invoice is paid. |
| `data[].invoices[].dueDate` | string | The due date of the invoice. |
| `data[].invoices[].number` | string | The number of the invoice. |
| `data[].invoices[].status` | string | The status of the invoice, returns draft, approved. |
| `data[].invoices[].updatedAt` | string | The UTC date and time when the invoice was last updated. |
| `data[].invoices[].uuid` | string | The unique identifier of the invoice. |
| `data[].jobCategoryUUID` | string | The unique identifier of the job category maintained in the job settings. |
| `data[].jobManagerUUID` | string | The unique identifier of the job's job manager. |
| `data[].jobNumber` | string | The number of the job. |
| `data[].jobStatusUUID` | string | The unique identifier of the job status maintained in the job settings. |
| `data[].milestones[].completed` | boolean | Indicate whether the milestone is completed. |
| `data[].milestones[].date` | string | The date of milestone. |
| `data[].milestones[].name` | string | The name of the milestone. |
| `data[].milestones[].phaseUUID` | string | The unique identifier of the milestone's phase. It can be mapped with the UUID in phases section. |
| `data[].name` | string | The name of the job. |
| `data[].notes[].createdAt` | string | The UTC date and time when the job note was created. |
| `data[].notes[].createdByUUID` | string | The unique identifier of the staff who created the job note. |
| `data[].notes[].date` | string | The date of the job note. |
| `data[].notes[].description` | string | The description of the job note. |
| `data[].notes[].phaseUUID` | string | The unique identifier of the job note's phase. It can be mapped with the UUID in phases section. |
| `data[].notes[].title` | string | The title of the job note. |
| `data[].notes[].updatedAt` | string | The UTC date and time when the job note was last updated. |
| `data[].notes[].uuid` | string | The unique identifier of the job note. |
| `data[].phases[].createdAt` | string | The UTC date and time when the job phase was created. |
| `data[].phases[].description` | string | The description of the job phase. |
| `data[].phases[].name` | string | The name of the job phase. |
| `data[].phases[].updatedAt` | string | The UTC date and time when the job phase was last updated. |
| `data[].phases[].uuid` | string | The unique identifier of the job phase. |
| `data[].priority` | string | The priority of the job, returns Low, Normal, High, Immediate. |
| `data[].purchaseOrders[].amountExTax` | number | The amount of the purchase order excluding tax. |
| `data[].purchaseOrders[].amountIncTax` | number | The amount of the purchase order including tax. |
| `data[].purchaseOrders[].billingStatus` | string | The billing status of the purchase order, returns awaiting, partial, full |
| `data[].purchaseOrders[].createdAt` | string | The UTC date and time when the purchase order was created. |
| `data[].purchaseOrders[].date` | string | The date of the purchase order. |
| `data[].purchaseOrders[].receivingStatus` | string | The receiving status of the purchase order, returns awaiting, partial, full |
| `data[].purchaseOrders[].status` | string | The general status of the purchase order, returns draft, issued, cancelled |
| `data[].purchaseOrders[].supplierUUID` | string | The unique identifier of the supplier associated with the purchase order. |
| `data[].purchaseOrders[].updatedAt` | string | The UTC date and time when the purchase order was last updated. |
| `data[].purchaseOrders[].uuid` | string | The unique identifier of the purchase order. |
| `data[].quotes[].amountExTax` | number | The amount excluding tax for the quote. |
| `data[].quotes[].amountIncTax` | number | The amount including tax for the quote. |
| `data[].quotes[].budget` | number | The budget of the quote. |
| `data[].quotes[].clientUUID` | string | The unique identifier of the client associated with the quote. |
| `data[].quotes[].contactUUID` | string | The unique identifier of the client contact associated with the quote. |
| `data[].quotes[].createdAt` | string | The UTC date and time when the quote was created. |
| `data[].quotes[].customFields[].name` | string | The name of the quote custom field. |
| `data[].quotes[].customFields[].uuid` | string | The unique identifier of the quote custom field. |
| `data[].quotes[].customFields[].value` | string | The value of the quote custom field. |
| `data[].quotes[].isMasterQuote` | boolean | Indicate whether it is a master quote of the job. |
| `data[].quotes[].name` | string | The name of the quote. |
| `data[].quotes[].number` | string | The number of the quote. |
| `data[].quotes[].salesPersonUUID` | string | The unique identifier of the sales person for the quote. |
| `data[].quotes[].status` | string | The status of the quote, returns draft, issued, accepted, declined, revised |
| `data[].quotes[].type` | string | The type of the quote, returns quote or estimate. |
| `data[].quotes[].updatedAt` | string | The UTC date and time when the quote was last updated. |
| `data[].quotes[].uuid` | string | The unique identifier of the quote. |
| `data[].quotes[].validFrom` | string | The date from when the quote is valid. |
| `data[].quotes[].validTo` | string | The date to when the quote is valid. |
| `data[].staffAssigned[].customBillableRate` | number | The custom billable rate of the staff for the job. It is only valid when the task invoice mode is Staff. |
| `data[].staffAssigned[].uuid` | string | The unique identifier of the staff who is assigned to the job. |
| `data[].startDate` | string | The start date of the job. |
| `data[].taskInvoiceRate` | string | The task invoice mode of the job, reflecting the job financial settings, returns staff or task. |
| `data[].tasks[].actualMinutes` | number | The actual time in minutes of the job task. |
| `data[].tasks[].billable` | boolean | Indicate whether the job task is billable. |
| `data[].tasks[].completed` | boolean | Indicate whether the job task has been completed. |
| `data[].tasks[].createdAt` | string | The UTC date time when the job task was created. |
| `data[].tasks[].customBillableRate` | number | The custom billable rate of the task for the job. It is only valid when the task invoice mode is Task. |
| `data[].tasks[].customFields[].name` | string | The name of the job task custom field. |
| `data[].tasks[].customFields[].uuid` | string | The unique identifier of the job task custom field. |
| `data[].tasks[].customFields[].value` | string | The value of the job task custom field. |
| `data[].tasks[].description` | string | The description of the job task. |
| `data[].tasks[].dueDate` | string | The due date of the job task. |
| `data[].tasks[].estimatedMinutes` | number | The estimated time in minutes of the job task. |
| `data[].tasks[].label` | string | The label of the job task. |
| `data[].tasks[].name` | string | The name of the job task. |
| `data[].tasks[].phaseUUID` | string | The unique identifier of the job task's phase. |
| `data[].tasks[].staff[].allocatedTime` | number |  |
| `data[].tasks[].staff[].uuid` | string |  |
| `data[].tasks[].startDate` | string | The start date of the job task. |
| `data[].tasks[].taskUUID` | string | The unique identifier of the task. |
| `data[].tasks[].updatedAt` | string | The UTC date time when the job task was last updated. |
| `data[].tasks[].uuid` | string | The unique identifier of the job task. |
| `data[].updatedAt` | string | The UTC date and time when the job was last updated. |
| `data[].uuid` | string | The unique identifier for the job. |
| `total` | number | The total number of jobs returned. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/jobs` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

