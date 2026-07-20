# WorkflowMax: Create Job Quote



```
POST https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-job-quote', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | The WorkflowMax job UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedDeclinedDate": "string",
      "amountExTax": 1,
      "amountIncTax": 1,
      "budget": 1,
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
          "unit_cost": 1,
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
          "uploadedBy": {
            "firstName": "Ava",
            "lastName": "Chen",
            "uuid": "string"
          },
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
          "phase": "string",
          "title": "string",
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "optionItemsExplanation": "string",
      "phases": {
        "1": {
          "createdAt": "string",
          "description": "string",
          "jobPhaseUUID": "string",
          "name": "Ava Chen",
          "order": 1,
          "updatedAt": "string",
          "uuid": "string"
        }
      },
      "quoteName": "Ava Chen",
      "quoteNumber": "string",
      "salesperson": {
        "firstName": "Ava",
        "lastName": "Chen",
        "uuid": "string"
      },
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedDeclinedDate` | string | The UTC date when the quote is accepted or declined. |
| `amountExTax` | number | The total amount of the quote excluding taxes. |
| `amountIncTax` | number | The total amount of the quote including taxes. |
| `budget` | number | The budget of the quote. |
| `client.email` | string | The email of the client associated with the quote. |
| `client.name` | string | The name of the client associated with the quote. |
| `client.phoneNumber` | string | The phone number of the client associated with the quote. |
| `client.uuid` | string | The unique identifier of the client associated with the quote. It can be mapped with the uuid in GET /clients/ endpoint. |
| `contact.email` | string | The email of the contact associated with the quote. |
| `contact.firstName` | string | The first name of the contact associated with the quote. |
| `contact.lastName` | string | The last name of the contact associated with the quote. |
| `contact.mobileNumber` | string | The mobile number of the contact associated with the quote. |
| `contact.phoneNumber` | string | The phone number of the contact associated with the quote. |
| `contact.uuid` | string | The unique identifier of the contact associated with the quote. It can be mapped with the uuid in GET /clients/contacts/ endpoint. |
| `costAmountExTax` | number | The cost amount of the quote excluding taxes. |
| `costs[].accepted` | boolean | Indicate whether the quote has been accepted. |
| `costs[].amount` | number | The total amount of the quote cost. |
| `costs[].billable` | boolean | Indicate whether the quote cost is billable. |
| `costs[].costCode` | string | The code of the quote cost. |
| `costs[].costNote` | string | The note of the quote cost. |
| `costs[].costUUID` | string | The unique identifier of the cost managed in the cost admin. It can be mapped with the uuid in GET /costs/ endpoint. |
| `costs[].createdAt` | string | The UTC date and time when the quote cost is created. |
| `costs[].description` | string | The description of the quote cost. |
| `costs[].fixedPrice` | boolean | Indicate whether the price of the quote cost is based on a fixed price. It is in calculated price if value is false. |
| `costs[].jobCostUUID` | string | The unique identifier of the job cost associated with the quote task. |
| `costs[].name` | string | The name of the quote cost. |
| `costs[].optional` | boolean | Indicate whether the quote cost is optional. |
| `costs[].order` | number | The order of the quote cost. |
| `costs[].quantity` | number | The quantity of the quote cost. |
| `costs[].quotePhaseUUID` | string | The unique identifier of the quote phase. It can be mapped with the uuid in phases section. |
| `costs[].tax[].taxName` | string | The name of the tax for the quote cost. |
| `costs[].tax[].taxRate` | number | The rate of the tax for the quote cost. |
| `costs[].type` | string | The type of the quote cost, e.g. service or stock. |
| `costs[].unit_cost` | number | The unit cost of the quote cost. |
| `costs[].unitPrice` | number | The unit price of the quote cost. |
| `costs[].updatedAt` | string | The UTC date and time when the quote cost is last updated. |
| `costs[].uuid` | string | The unique identifier of the quote cost. |
| `createdAt` | string | The UTC date and time when the quote is created. |
| `customFields[].name` | string | The name of the quote custom field. |
| `customFields[].uuid` | string | The unique identifier of the quote custom field. |
| `customFields[].value` | string | The value of the quote custom field. |
| `description` | string | The description of the quote. |
| `documents[].createdAt` | string | The UTC date and time when the quote document is firstly uploaded. |
| `documents[].downloadURL` | string | The downloadURL of the quote document. |
| `documents[].fileName` | string | The file name of the quote document. |
| `documents[].fileSize` | number | The file size of the quote document. |
| `documents[].note` | string | The note of the quote document. |
| `documents[].phase` | string | The phase of the quote document. |
| `documents[].title` | string | The title of the quote document. |
| `documents[].updatedAt` | string | The UTC date and time when the quote document is last updated. |
| `documents[].uploadedBy.firstName` | string | The first name of the staff who uploaded the quote document. |
| `documents[].uploadedBy.lastName` | string | The last name of the staff who uploaded the quote document. |
| `documents[].uploadedBy.uuid` | string | The unique identifier of the staff who uploaded the quote document. It can be mapped with the uuid in the GET /staff/ endpoint. |
| `documents[].uuid` | string | The unique identifier of the quote document. |
| `fixedPrice` | boolean | Indicate whether the price of the quote is based on a fixed price. It is in calculated price if value is false. |
| `job.number` | string | The number of the job associated with the quote. |
| `job.uuid` | string | The unique identifier of the job associated with the quote. |
| `jobMasterQuote` | boolean | Indicate whether the quote is the master quote of the job. |
| `lead.name` | string | The name of the lead associated with the quote. |
| `lead.uuid` | string | The unique identifier of the lead associated with the quote. |
| `notes[].comments[].comment` | string | The details of the note comment. |
| `notes[].comments[].createdAt` | string | The date and time when the note comment is created. |
| `notes[].comments[].createdBy.firstName` | string | The first name of the staff who added the note comment. |
| `notes[].comments[].createdBy.lastName` | string | The last name of the staff who added the note comment. |
| `notes[].comments[].createdBy.uuid` | string | The unique identifier of the staff who added the note comment. |
| `notes[].comments[].updatedAt` | string | The date and time when the note comment is last updated. |
| `notes[].createdAt` | string | The UTC date and time when the quote note is created. |
| `notes[].createdBy.firstName` | string | The first name of the staff who created the quote note. |
| `notes[].createdBy.lastName` | string | The last name of the staff who created the quote note. |
| `notes[].createdBy.uuid` | string | The unique identifier of the staff who created the quote note. It can be mapped with the uuid in the GET /staff/ endpoint. |
| `notes[].date` | string | The UTC date of the quote note. |
| `notes[].description` | string | The description of the quote note. |
| `notes[].phase` | string | The phase of the quote note. |
| `notes[].title` | string | The title of the quote note. |
| `notes[].updatedAt` | string | The UTC date and time when the quote note is last updated. |
| `notes[].uuid` | string | The unique identifier of the quote note. |
| `optionItemsExplanation` | string | The optional items explanation of the quote. |
| `phases.1.createdAt` | string | The UTC date and time when the quote phase is created. |
| `phases.1.description` | string | The description of the quote phase. |
| `phases.1.jobPhaseUUID` | string | The unique identifier of the job phase associated with the quote phase. |
| `phases.1.name` | string | The name of the quote phase. |
| `phases.1.order` | number | The order of the quote phase. |
| `phases.1.updatedAt` | string | The UTC date and time when the quote phase is last updated. |
| `phases.1.uuid` | string | The unique identifier of the quote phase. |
| `quoteName` | string | The name of the quote. |
| `quoteNumber` | string | The number of the quote. |
| `salesperson.firstName` | string | The first name of the sales person of the quote. |
| `salesperson.lastName` | string | The last name of the sales person of the quote. |
| `salesperson.uuid` | string | The unique identifier of the sales person of the quote. It can be mapped with the uuid in GET /staff/ endpoint. |
| `sent` | boolean | Indicate whether the quote has been sent to the customer. |
| `status` | string | The status of the quote, e.g. draft, issued, declined, accepted, revised. |
| `tasks[].accepted` | boolean | Indicate whether the quote task is accepted. |
| `tasks[].amount` | number | The price amount of the quote task. |
| `tasks[].baseRate` | number | Returns when staffRate is false. The base rate of the quote task. |
| `tasks[].billable` | boolean | Indicate whether the quote task is billable. |
| `tasks[].billableRate` | number | Returns when staffRate is false. The billable rate of the quote task. |
| `tasks[].costAmount` | number | The cost amount of the quote task. |
| `tasks[].createdAt` | string | The UTC date and time when the quote task is created. |
| `tasks[].description` | string | The description of the quote task. |
| `tasks[].fixedPrice` | boolean | Indicate whether the price of the quote task is based on a fixed price. It is in calculated price if value is false. |
| `tasks[].jobTaskUUID` | string | The unique identifier of the job task associated with the quote task. |
| `tasks[].label` | string | The label of the quote task. |
| `tasks[].name` | string | The name of the quote task. |
| `tasks[].optional` | boolean | Indicate whether the quote task is optional. |
| `tasks[].order` | number | The price amount of the quote task. |
| `tasks[].quotePhaseUUID` | string | The unique identifier of the quote phase. It can be mapped with the uuid in phases section. |
| `tasks[].staff[].baseRate` | string | The base rate of the staff for the quote task. |
| `tasks[].staff[].billableRate` | string | The billable rate of the staff for the quote task. |
| `tasks[].staff[].time` | string | Allocated time in minutes of the staff for the quote task. |
| `tasks[].staff[].uuid` | string | The unique identifier of the organization user. |
| `tasks[].staffRates` | boolean | Indicate whether there is staff allocation for the quote task. |
| `tasks[].taskUUID` | string | The unique identifier of the task as managed in the task admin. It can be mapped with the uuid in GET /tasks/ endpoint. |
| `tasks[].tax[].taxName` | string | The name of the task for the quote task. |
| `tasks[].tax[].taxRate` | number | The rate of the tax for the quote task. |
| `tasks[].time` | number | The estimated time of the quote task. |
| `tasks[].updatedAt` | string | The UTC date and time when the quote task is last updated. |
| `tasks[].uuid` | string | The unique identifier of the quote task. |
| `type` | string | The type of the quote, e.g. quote or estimate. |
| `updatedAt` | string | The UTC date and time when the quote is last updated. |
| `uuid` | string | The unique identifier of the quote. |
| `validFrom` | string | The date from when the quote is valid. |
| `validTo` | string | The date to when the quote is valid. |

## Native endpoint

Through the native WorkflowMax API, this operation is `POST v2/jobs/{UUID}/quotes` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-quote.md) for the provider-specific parameters and requirements.

