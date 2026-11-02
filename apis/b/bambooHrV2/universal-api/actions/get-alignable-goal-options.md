# BambooHR: Get Alignable Goal Options

Retrieves alignable goal options from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-alignable-goal-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-alignable-goal-options?connectionId=$CONNECTION_ID&employeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-alignable-goal-options?${params}`, {
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
| `employeeId` | string | yes | The internal employee ID of the employee whose alignable goal options are returned. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `goalId` | number | no | Optional goal ID whose current alignment should be included in the results. Only pass a goal ID that belongs to the specified employee. If this endpoint returns 403 for an otherwise visible goal, report that alignment options are restricted by permissions rather than treating the goal ID as invalid. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/performance/employees/:employeeId/goals/alignmentOptions` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alignable-goal-options.md) for the provider-specific parameters and requirements.

