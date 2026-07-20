# Week Plan: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-current-user?connectionId=$CONNECTION_ID&Day=1&Month=1&Timezone=1&TzName=Ava%20Chen&Year=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "Day": "1",
  "Month": "1",
  "Timezone": "1",
  "TzName": "Ava Chen",
  "Year": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-current-user?${params}`, {
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
| `Day` | number | yes | Calendar day used by the Week Plan user endpoint. |
| `Month` | number | yes | Calendar month used by the Week Plan user endpoint. |
| `Timezone` | number | yes | Timezone offset in minutes used by the Week Plan user endpoint. |
| `TzName` | string | yes | IANA timezone name used by the Week Plan user endpoint. |
| `Year` | number | yes | Calendar year used by the Week Plan user endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionLists": [
        {}
      ],
      "Changes": [
        {}
      ],
      "GlobalFeatures": [
        "string"
      ],
      "User": {},
      "WeekPlanDto": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionLists` | array<object> |  |
| `Changes` | array<object> |  |
| `GlobalFeatures` | array<string> |  |
| `User` | object |  |
| `WeekPlanDto` | object |  |

## Native endpoint

Through the native Week Plan API, this operation is `GET users` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

