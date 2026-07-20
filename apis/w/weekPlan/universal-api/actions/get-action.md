# Week Plan: Get Action



```
GET https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-action?connectionId=$CONNECTION_ID&actionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-action?${params}`, {
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
| `actionId` | number | yes | Action ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionId": 1,
      "CompletedSubTasksCount": 1,
      "Date": "string",
      "EndDate": "string",
      "GoalId": 1,
      "HtmlText": "string",
      "IsCompleted": true,
      "IsDeleted": true,
      "NotesHtml": "string",
      "ParentActionId": 1,
      "Quadrant": 1,
      "StartDate": "string",
      "SubTasksCount": 1,
      "Text": "string",
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
| `CompletedSubTasksCount` | number |  |
| `Date` | string |  |
| `EndDate` | string |  |
| `GoalId` | number |  |
| `HtmlText` | string |  |
| `IsCompleted` | boolean |  |
| `IsDeleted` | boolean |  |
| `NotesHtml` | string |  |
| `ParentActionId` | number |  |
| `Quadrant` | number |  |
| `StartDate` | string |  |
| `SubTasksCount` | number |  |
| `Text` | string |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `GET actions/:actionId` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action.md) for the provider-specific parameters and requirements.

