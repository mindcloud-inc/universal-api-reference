# WorkflowMax: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-tasks?${params}`, {
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
          "baseRate": 1,
          "billableRate": 1,
          "createdAt": "string",
          "customClientRates": [
            {
              "billableRate": 1,
              "clientUUID": "string"
            }
          ],
          "customStaffRates": [
            {
              "baseRate": 1,
              "billableRate": 1,
              "staffUUID": "string"
            }
          ],
          "deletedAt": "string",
          "description": "string",
          "exportCode": "string",
          "historicRates": [
            {
              "appliedUpTo": "string",
              "billableRate": 1
            }
          ],
          "incomeAccount": "string",
          "name": "Ava Chen",
          "salesTax": [
            {
              "name": "Ava Chen",
              "rate": 1
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
| `data[].baseRate` | number | The base rate set for the task. |
| `data[].billableRate` | number | The billable rate set for the task. |
| `data[].createdAt` | string | The date and time when the task was created. |
| `data[].customClientRates[].billableRate` | number | The custom billable rate applied to the task for this client. |
| `data[].customClientRates[].clientUUID` | string | The unique identifier of the client with a custom rate applied to the task. |
| `data[].customStaffRates[].baseRate` | number | The custom base rate applied to the task for this staff member. |
| `data[].customStaffRates[].billableRate` | number | The custom billable rate applied to the task for this staff member. |
| `data[].customStaffRates[].staffUUID` | string | Unique identifier for the staff member assigned to the task. |
| `data[].deletedAt` | string | The date and time when the task was deleted. |
| `data[].description` | string | The detailed description of the task. |
| `data[].exportCode` | string | Code used for exporting the task data. |
| `data[].historicRates[].appliedUpTo` | string | The date up to which the historical rate has been applied. |
| `data[].historicRates[].billableRate` | number | The historical billable rate for the task. |
| `data[].incomeAccount` | string | The income account associated with the task. |
| `data[].name` | string | The name of the task. |
| `data[].salesTax[].name` | string | The name of the sales tax. |
| `data[].salesTax[].rate` | number | The tax rate of the sales tax. |
| `data[].updatedAt` | string | The date and time when the task was last updated. |
| `data[].uuid` | string | The unique identifier of the task. |
| `total` | number | The total number of tasks returned. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/tasks` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

