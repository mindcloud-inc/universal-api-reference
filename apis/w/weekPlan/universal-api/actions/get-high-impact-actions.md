# Week Plan: Get High Impact Actions



```
GET https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-high-impact-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-high-impact-actions?connectionId=$CONNECTION_ID&week=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "week": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-high-impact-actions?${params}`, {
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
| `week` | string | yes | A date inside the requested week in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionId": 1,
      "EndDate": "string",
      "GoalId": 1,
      "HtmlText": "string",
      "IsCompleted": true,
      "IsDeleted": true,
      "Quadrant": 1,
      "RoleId": 1,
      "StartDate": "string",
      "Text": "string",
      "WeekDate": "string",
      "WorkspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionId` | number |  |
| `EndDate` | string |  |
| `GoalId` | number |  |
| `HtmlText` | string |  |
| `IsCompleted` | boolean |  |
| `IsDeleted` | boolean |  |
| `Quadrant` | number |  |
| `RoleId` | number |  |
| `StartDate` | string |  |
| `Text` | string |  |
| `WeekDate` | string |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `GET actions/hits` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-high-impact-actions.md) for the provider-specific parameters and requirements.

