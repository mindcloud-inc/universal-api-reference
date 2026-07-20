# WorkflowMax: List Job Costs



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-job-costs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-job-costs?connectionId=$CONNECTION_ID&limit=25&offset=0&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-job-costs?${params}`, {
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
| `jobId` | string | yes | The WorkflowMax job UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
          "description": "string",
          "note": "string",
          "phase": {
            "name": "Ava Chen",
            "uuid": "string"
          },
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
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].actual` | boolean | Indicate whether the job cost is actual, it is an estimate cost if value is false. |
| `data[].billable` | boolean | Indicate whether the job cost is billable. |
| `data[].costCode` | string | The cost code of the job cost. |
| `data[].costUUID` | string | The unique identifier of the cost as managed in the organization settings. |
| `data[].createdAt` | string | The UTC date and time when the job cost was created. |
| `data[].customFields[].name` | string | The name of the job cost custom field. |
| `data[].customFields[].uuid` | string | The unique identifier of the job cost custom field. |
| `data[].customFields[].value` | string | The value of the job cost custom field. |
| `data[].date` | string | The date of the job cost. |
| `data[].description` | string | The description of the job cost. |
| `data[].note` | string | The cost note of the job cost. |
| `data[].phase.name` | string | The name of the phase for the job cost. |
| `data[].phase.uuid` | string | The unique identifier of the phase for the job cost. |
| `data[].quantity` | number | The quantity of the job cost. |
| `data[].supplier.name` | string | The name of the supplier. |
| `data[].supplier.uuid` | string | The unique identifier of the supplier for the job cost. |
| `data[].type` | string | The type of the job cost, returns service or stock. |
| `data[].unitCost` | number | The unit cost of the job cost. |
| `data[].unitPrice` | number | The unit price of the job cost. |
| `data[].updatedAt` | string | The UTC date and time when the job cost was last updated. |
| `data[].uuid` | string | The unique identifier of the job cost. |
| `total` | number | The total number of job costs returned. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/jobs/{UUID}/costs` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-job-costs.md) for the provider-specific parameters and requirements.

