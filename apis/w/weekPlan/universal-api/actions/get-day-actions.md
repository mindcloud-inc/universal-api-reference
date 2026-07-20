# Week Plan: Get Day Actions



```
GET https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-day-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-day-actions?connectionId=$CONNECTION_ID&Day=1&Month=1&workspaceId=1&Year=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "Day": "1",
  "Month": "1",
  "workspaceId": "1",
  "Year": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-day-actions?${params}`, {
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
| `Day` | number | yes | Calendar day of month for the requested day. |
| `Month` | number | yes | Calendar month for the requested day. |
| `workspaceId` | number | yes | The workspace to read actions from. |
| `Year` | number | yes | Calendar year for the requested day. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionId": 1,
      "ActionListId": 1,
      "Date": "string",
      "EndDate": "string",
      "HtmlText": "string",
      "IsCompleted": true,
      "IsDeleted": true,
      "MeetingId": 1,
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
| `ActionListId` | number |  |
| `Date` | string |  |
| `EndDate` | string |  |
| `HtmlText` | string |  |
| `IsCompleted` | boolean |  |
| `IsDeleted` | boolean |  |
| `MeetingId` | number |  |
| `Quadrant` | number |  |
| `RoleId` | number |  |
| `StartDate` | string |  |
| `Text` | string |  |
| `WeekDate` | string |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `GET actions/day` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-day-actions.md) for the provider-specific parameters and requirements.

