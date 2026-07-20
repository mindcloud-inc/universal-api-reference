# WorkflowMax: Get Task



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-task?${params}`, {
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseRate` | number | The base rate set for the task. |
| `billableRate` | number | The billable rate set for the task. |
| `createdAt` | string | The UTC date and time when the task was created. |
| `customClientRates[].billableRate` | number | The custom billable rate applied to the task for this client. |
| `customClientRates[].clientUUID` | string | The unique identifier of the client with a custom rate applied to the task. |
| `customStaffRates[].baseRate` | number | The custom base rate applied to the task for this staff member. |
| `customStaffRates[].billableRate` | number | The custom billable rate applied to the task for this staff member. |
| `customStaffRates[].staffUUID` | string | The unique identifier of the staff member with a custom rate applied to the task. |
| `deletedAt` | string | The UTC date and time when the task was deleted. |
| `description` | string | The detailed description of the task. |
| `exportCode` | string | Code used for exporting the task data. |
| `historicRates[].appliedUpTo` | string | The date up to which the historical rate has been applied. |
| `historicRates[].billableRate` | number | The historical billable rate for the task. |
| `incomeAccount` | string | The income account associated with the task. |
| `name` | string | The name of the task. |
| `salesTax[].name` | string | The name of the sales tax. |
| `salesTax[].rate` | number | The tax rate of the sales tax. |
| `updatedAt` | string | The UTC date and time when the task was last updated. |
| `uuid` | string | The unique identifier of the task. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/tasks/{UUID}` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

