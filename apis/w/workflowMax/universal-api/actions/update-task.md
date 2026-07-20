# WorkflowMax: Update Task



```
PUT https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The WorkflowMax task UUID. |

## Response

```json
{
  "success": true,
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
      "taxes": [
        {
          "name": "Ava Chen",
          "rate": 1
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
| `baseRate` | number | The base rate of the task. |
| `billableRate` | number | The billable rate of the task. |
| `createdAt` | string | The UTC timestamp indicating when the task was created. |
| `customClientRates[].billableRate` | number | The custom billable rate of the client custom rate. |
| `customClientRates[].clientUUID` | string | The unique identifier of the client. |
| `customStaffRates[].baseRate` | number | The custom base rate of the staff custom rate. |
| `customStaffRates[].billableRate` | number | The custom billable rate of the staff custom rate. |
| `customStaffRates[].staffUUID` | string | The unique identifier of the staff. |
| `deletedAt` | string | The UTC timestamp indicating when the task was deleted. |
| `description` | string | The detailed information of the task. |
| `exportCode` | string | The export code of the task. |
| `historicRates[].appliedUpTo` | string | The date up to which the historical rate is applied. |
| `historicRates[].billableRate` | number | The historical billable rate of the task. |
| `incomeAccount` | string | The unique identifier of the income account for the task. |
| `name` | string | The name of the task. |
| `taxes[].name` | string | The name of the tax. |
| `taxes[].rate` | number | The rate of the tax. |
| `updatedAt` | string | The UTC timestamp indicating when the task was last updated. |
| `uuid` | string | The unique identifier of the task. |

## Native endpoint

Through the native WorkflowMax API, this operation is `PUT v2/tasks/{UUID}` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

