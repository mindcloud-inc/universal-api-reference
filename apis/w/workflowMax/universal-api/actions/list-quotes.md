# WorkflowMax: List Quotes



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-quotes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-quotes?${params}`, {
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
          "acceptedDeclinedDate": "string",
          "amountExTax": 1,
          "amountIncTax": 1,
          "budget": 1,
          "clientUUID": "string",
          "contactUUID": "string",
          "costAmountExTax": 1,
          "costs": [
            {
              "accepted": true,
              "amount": 1,
              "billable": true,
              "costCode": "string",
              "costNote": "string",
              "costUUID": "string",
              "createdAt": "string",
              "description": "string",
              "fixedPrice": true,
              "jobCostUUID": "string",
              "name": "Ava Chen",
              "optional": true,
              "order": 1,
              "quantity": 1,
              "quotePhaseUUID": "string",
              "tax": [
                {
                  "taxName": "Ava Chen",
                  "taxRate": 1
                }
              ],
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
          "description": "string",
          "documents": [
            {
              "createdAt": "string",
              "downloadURL": "https://example.com",
              "fileName": "Ava Chen",
              "fileSize": 1,
              "note": "string",
              "phase": "string",
              "title": "string",
              "updatedAt": "string",
              "uploadedByUUID": "string",
              "uuid": "string"
            }
          ],
          "fixedPrice": true,
          "job": {
            "number": "string",
            "uuid": "string"
          },
          "jobMasterQuote": true,
          "lead": {
            "name": "Ava Chen",
            "uuid": "string"
          },
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
          "optionalItemsExplanation": "string",
          "phases": [
            {
              "createdAt": "string",
              "description": "string",
              "jobPhaseUUID": "string",
              "name": "Ava Chen",
              "order": 1,
              "updatedAt": "string",
              "uuid": "string"
            }
          ],
          "quoteName": "Ava Chen",
          "quoteNumber": "string",
          "salespersonUUID": "string",
          "sent": true,
          "status": "string",
          "tasks": [
            {
              "accepted": true,
              "amount": 1,
              "baseRate": 1,
              "billable": true,
              "billableRate": 1,
              "costAmount": 1,
              "createdAt": "string",
              "description": "string",
              "fixedPrice": true,
              "jobTaskUUID": "string",
              "label": "string",
              "name": "Ava Chen",
              "optional": true,
              "order": 1,
              "quotePhaseUUID": "string",
              "staff": [
                {
                  "baseRate": "string",
                  "billableRate": "string",
                  "time": "string",
                  "uuid": "string"
                }
              ],
              "staffRates": true,
              "taskUUID": "string",
              "tax": [
                {
                  "taxName": "Ava Chen",
                  "taxRate": 1
                }
              ],
              "time": 1,
              "updatedAt": "string",
              "uuid": "string"
            }
          ],
          "type": "string",
          "updatedAt": "string",
          "uuid": "string",
          "validFrom": "string",
          "validTo": "string"
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
| `data[].acceptedDeclinedDate` | string | The UTC date and time when the quote is accepted or declined. |
| `data[].amountExTax` | number | The total amount of the quote excluding taxes. |
| `data[].amountIncTax` | number | The total amount of the quote including taxes. |
| `data[].budget` | number | The budget of the quote. |
| `data[].clientUUID` | string | The unique identifier of the client associated with the quote. It can be mapped with the uuid in GET /clients/ endpoint. |
| `data[].contactUUID` | string | The unique identifier of the contact associated with the quote. It can be mapped with the uuid in GET /clients/contacts/ endpoint. |
| `data[].costAmountExTax` | number | The cost amount of the quote excluding taxes. |
| `data[].costs[].accepted` | boolean | Indicate whether the quote has been accepted. |
| `data[].costs[].amount` | number | The total amount of the quote cost. |
| `data[].costs[].billable` | boolean | Indicate whether the quote cost is billable. |
| `data[].costs[].costCode` | string | The code of the quote cost. |
| `data[].costs[].costNote` | string | The note of the quote cost. |
| `data[].costs[].costUUID` | string | The unique identifier of the cost managed in the cost admin. It can be mapped with the uuid in GET /costs/ endpoint. |
| `data[].costs[].createdAt` | string | The UTC date and time when the quote cost is created. |
| `data[].costs[].description` | string | The description of the quote cost. |
| `data[].costs[].fixedPrice` | boolean | Indicate whether the price of the quote cost is based on a fixed price. It is in calculated price if value is false. |
| `data[].costs[].jobCostUUID` | string | The unique identifier of the job cost associated with the quote task. |
| `data[].costs[].name` | string | The name of the quote cost. |
| `data[].costs[].optional` | boolean | Indicate whether the quote cost is optional. |
| `data[].costs[].order` | number | The order of the quote cost. |
| `data[].costs[].quantity` | number | The quantity of the quote cost. |
| `data[].costs[].quotePhaseUUID` | string | The unique identifier of the quote phase. It can be mapped with the uuid in phases section. |
| `data[].costs[].tax[].taxName` | string | The name of the tax for the quote cost. |
| `data[].costs[].tax[].taxRate` | number | The rate of the tax for the quote cost. |
| `data[].costs[].type` | string | The type of the quote cost, e.g. service or stock. |
| `data[].costs[].unitCost` | number | The unit cost of the quote cost. |
| `data[].costs[].unitPrice` | number | The unit price of the quote cost. |
| `data[].costs[].updatedAt` | string | The UTC date and time when the quote cost is last updated. |
| `data[].costs[].uuid` | string | The unique identifier of the quote cost. |
| `data[].createdAt` | string | The UTC date and time when the quote is created. |
| `data[].customFields[].name` | string | The name of the quote custom field. |
| `data[].customFields[].uuid` | string | The unique identifier of the quote custom field. |
| `data[].customFields[].value` | string | The value of the quote custom field. |
| `data[].description` | string | The description of the quote. |
| `data[].documents[].createdAt` | string | The UTC date and time when the quote document is firstly uploaded. |
| `data[].documents[].downloadURL` | string | The downloadURL of the quote document. |
| `data[].documents[].fileName` | string | The file name of the quote document. |
| `data[].documents[].fileSize` | number | The file size of the quote document. |
| `data[].documents[].note` | string | The note of the quote document. |
| `data[].documents[].phase` | string | The phase of the quote document. |
| `data[].documents[].title` | string | The title of the quote document. |
| `data[].documents[].updatedAt` | string | The UTC date and time when the quote document is last updated. |
| `data[].documents[].uploadedByUUID` | string | The unique identifier of the staff who uploaded the quote document. It can be mapped with the uuid in the GET /staff/ endpoint. |
| `data[].documents[].uuid` | string | The unique identifier of the quote document. |
| `data[].fixedPrice` | boolean | Indicate whether the price of the quote is based on a fixed price. It is in calculated price if value is false. |
| `data[].job.number` | string | The number of the job associated with the quote. |
| `data[].job.uuid` | string | The unique identifier of the job associated with the quote. |
| `data[].jobMasterQuote` | boolean | Indicate whether the quote is the master quote of the job. |
| `data[].lead.name` | string | The name of the lead associated with the quote. |
| `data[].lead.uuid` | string | The unique identifier of the lead associated with the quote. |
| `data[].notes[].createdAt` | string | The UTC date and time when the quote note is created. |
| `data[].notes[].createdByUUID` | string | The unique identifier of the staff who created the quote note. It can be mapped with the uuid in the GET /staff/ endpoint. |
| `data[].notes[].date` | string | The UTC date of the quote note. |
| `data[].notes[].description` | string | The description of the quote note. |
| `data[].notes[].phase` | string | The phase of the quote note. |
| `data[].notes[].title` | string | The title of the quote note. |
| `data[].notes[].updatedAt` | string | The UTC date and time when the quote note is last updated. |
| `data[].notes[].uuid` | string | The unique identifier of the quote note. |
| `data[].optionalItemsExplanation` | string | The optional items explanation of the quote. |
| `data[].phases[].createdAt` | string | The UTC date and time when the quote phase is created. |
| `data[].phases[].description` | string | The description of the quote phase. |
| `data[].phases[].jobPhaseUUID` | string | The unique identifier of the job phase associated with the quote phase. |
| `data[].phases[].name` | string | The name of the quote phase. |
| `data[].phases[].order` | number | The order of the quote phase. |
| `data[].phases[].updatedAt` | string | The UTC date and time when the quote phase is last updated. |
| `data[].phases[].uuid` | string | The unique identifier of the quote phase. |
| `data[].quoteName` | string | The name of the quote. |
| `data[].quoteNumber` | string | The number of the quote. |
| `data[].salespersonUUID` | string | The unique identifier of the sales person of the quote. It can be mapped with the uuid in GET /staff/ endpoint. |
| `data[].sent` | boolean | Indicate whether the quote has been sent to the customer. |
| `data[].status` | string | The status of the quote, e.g. draft, issued, declined, accepted, revised. |
| `data[].tasks[].accepted` | boolean | Indicate whether the quote task is accepted. |
| `data[].tasks[].amount` | number | The price amount of the quote task. |
| `data[].tasks[].baseRate` | number | Returns when staffRate is false. The base rate of the quote task. |
| `data[].tasks[].billable` | boolean | Indicate whether the quote task is billable. |
| `data[].tasks[].billableRate` | number | Returns when staffRate is false. The billable rate of the quote task. |
| `data[].tasks[].costAmount` | number | The cost amount of the quote task. |
| `data[].tasks[].createdAt` | string | The UTC date and time when the quote task is created. |
| `data[].tasks[].description` | string | The description of the quote task. |
| `data[].tasks[].fixedPrice` | boolean | Indicate whether the price of the quote task is based on a fixed price. It is in calculated price if value is false. |
| `data[].tasks[].jobTaskUUID` | string | The unique identifier of the job task associated with the quote task. |
| `data[].tasks[].label` | string | The label of the quote task. |
| `data[].tasks[].name` | string | The name of the quote task. |
| `data[].tasks[].optional` | boolean | Indicate whether the quote task is optional. |
| `data[].tasks[].order` | number | The order of the quote task. |
| `data[].tasks[].quotePhaseUUID` | string | The unique identifier of the quote phase. It can be mapped with the uuid in phases section. |
| `data[].tasks[].staff[].baseRate` | string | The base rate of the staff for the quote task. |
| `data[].tasks[].staff[].billableRate` | string | The billable rate of the staff for the quote task. |
| `data[].tasks[].staff[].time` | string | Allocated time in minutes of the staff for the quote task. |
| `data[].tasks[].staff[].uuid` | string | The unique identifier of the organization user. |
| `data[].tasks[].staffRates` | boolean | Indicate whether there is staff allocation for the quote task. |
| `data[].tasks[].taskUUID` | string | The unique identifier of the task as managed in the task admin. It can be mapped with the uuid in GET /tasks/ endpoint. |
| `data[].tasks[].tax[].taxName` | string | The name of the task for the quote task. |
| `data[].tasks[].tax[].taxRate` | number | The rate of the tax for the quote task. |
| `data[].tasks[].time` | number | The estimated time of the quote task. |
| `data[].tasks[].updatedAt` | string | The UTC date and time when the quote task is last updated. |
| `data[].tasks[].uuid` | string | The unique identifier of the quote task. |
| `data[].type` | string | The type of the quote, e.g. quote or estimate. |
| `data[].updatedAt` | string | The UTC date and time when the quote is last updated. |
| `data[].uuid` | string | The unique identifier of the quote. |
| `data[].validFrom` | string | The date from when the quote is valid. |
| `data[].validTo` | string | The date to when the quote is valid. |
| `total` | number | The total number of quotes returned. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/quotes` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-quotes.md) for the provider-specific parameters and requirements.

