# WorkflowMax: List Timesheets



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-timesheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-timesheets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-timesheets?${params}`, {
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
          "endTime": "string",
          "job": {
            "jobNumber": "string",
            "name": "Ava Chen",
            "uuid": "string"
          },
          "jobTask": {
            "label": "string",
            "name": "Ava Chen",
            "uuid": "string"
          },
          "note": "string",
          "staff": {
            "firstName": "Ava",
            "lastName": "Chen",
            "uuid": "string"
          },
          "startTime": "string",
          "submittedAt": "string",
          "time": 1,
          "updatedAt": "string",
          "uuid": "string",
          "wip": {
            "baseRate": 1,
            "chargeAmount": 1,
            "chargeRate": 1,
            "costAmount": 1,
            "invoice": {
              "invoiceAmount": 1,
              "invoiceDate": "string",
              "invoiceRate": 1,
              "invoiceTaskUUID": "string",
              "invoiceTime": 1,
              "invoiceUUID": "string",
              "writeonAmount": 1
            },
            "standardAmount": 1,
            "standardRate": 1
          }
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
| `data[].billable` | boolean | Indicates if the timesheet entry is billable. |
| `data[].createdAt` | string | The UTC date and time when the timesheet was created. |
| `data[].customFields[].name` | string | The name for the timesheet entry's custom field. |
| `data[].customFields[].uuid` | string | The unique identifier for the timesheet entry's custom field. |
| `data[].customFields[].value` | string | The value for the timesheet entry's custom field. |
| `data[].date` | string | The date of the timesheet entry. |
| `data[].endTime` | string | The end time of the timesheet entry. Only populate when have value. |
| `data[].job.jobNumber` | string | The job number of the job associated with the timesheet entry. |
| `data[].job.name` | string | The job name of the job associated with the timesheet entry. |
| `data[].job.uuid` | string | The unique identifier of the job associated with the timesheet entry. |
| `data[].jobTask.label` | string | The label of the job task associated with the timesheet entry. |
| `data[].jobTask.name` | string | The name of the job task associated with the timesheet entry. |
| `data[].jobTask.uuid` | string | The unique identifier of the job task associated with the timesheet entry. |
| `data[].note` | string | Additional notes or comments related to the timesheet entry. |
| `data[].staff.firstName` | string | The first name of the staff associated with the timesheet entry. |
| `data[].staff.lastName` | string | The last name of the staff associated with the timesheet entry. |
| `data[].staff.uuid` | string | The unique identifier of the staff associated with the timesheet entry. |
| `data[].startTime` | string | The start time of the timesheet entry. Only populate when have value. |
| `data[].submittedAt` | string | The UTC date and time when the timesheet entry was submitted. |
| `data[].time` | number | The time in minutes of the timesheet entry. |
| `data[].updatedAt` | string | The UTC date and time when the timesheet was last updated. |
| `data[].uuid` | string | The unique identifier of the timesheet entry. |
| `data[].wip.baseRate` | number | The base rate of the timesheet. |
| `data[].wip.chargeAmount` | number | The total charge amount of the timesheet. |
| `data[].wip.chargeRate` | number | The charge rate of the timesheet. |
| `data[].wip.costAmount` | number | The total cost amount of the timesheet. |
| `data[].wip.invoice.invoiceAmount` | number | The total invoiced amount of the timesheet. |
| `data[].wip.invoice.invoiceDate` | string | The date of the invoice. |
| `data[].wip.invoice.invoiceRate` | number | The invoice rate of the timesheet. |
| `data[].wip.invoice.invoiceTaskUUID` | string | The unique identifier of the invoice task associated with the timesheet. |
| `data[].wip.invoice.invoiceTime` | number | The invoiced time in minutes of the timesheet. |
| `data[].wip.invoice.invoiceUUID` | string | The unique identifier of the invoice. |
| `data[].wip.invoice.writeonAmount` | number | The writeon amount of the timesheet. Negative amount refers to write off and positive amount refers to write on amount. |
| `data[].wip.standardAmount` | number | The total standard amount of the timesheet. |
| `data[].wip.standardRate` | number | The standard rate of the timesheet. |
| `total` | number | The total number of timesheets returned in the response. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/timesheets` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-timesheets.md) for the provider-specific parameters and requirements.

