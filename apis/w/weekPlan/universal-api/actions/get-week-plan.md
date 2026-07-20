# Week Plan: Get Week Plan



```
GET https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-week-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-week-plan?connectionId=$CONNECTION_ID&Day=1&Month=1&WorkspaceId=1&Year=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "Day": "1",
  "Month": "1",
  "WorkspaceId": "1",
  "Year": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-week-plan?${params}`, {
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
| `Day` | number | yes | Calendar day used to anchor the requested week. |
| `Month` | number | yes | Calendar month for the requested week. |
| `WorkspaceId` | number | yes | The workspace to read the week plan for. |
| `Year` | number | yes | Calendar year for the requested week. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Actions": [
        {}
      ],
      "CurrentWeek": {},
      "NextWeek": {},
      "PreviousWeek": {},
      "WeekDays": [
        {}
      ],
      "WeeklyRoles": [
        {}
      ],
      "WeekNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Actions` | array<object> |  |
| `CurrentWeek` | object |  |
| `NextWeek` | object |  |
| `PreviousWeek` | object |  |
| `WeekDays` | array<object> |  |
| `WeeklyRoles` | array<object> |  |
| `WeekNumber` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `GET plans` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-week-plan.md) for the provider-specific parameters and requirements.

