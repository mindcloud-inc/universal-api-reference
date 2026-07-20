# Week Plan: Get Lists



```
GET https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-lists?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-lists?${params}`, {
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
| `workspaceId` | number | yes | The workspace to read lists from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionListId": 1,
      "AutoPromoteToToday": true,
      "BoardName": "Ava Chen",
      "IsPending": true,
      "Name": "Ava Chen",
      "Order": 1,
      "WorkspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionListId` | number |  |
| `AutoPromoteToToday` | boolean |  |
| `BoardName` | string |  |
| `IsPending` | boolean |  |
| `Name` | string |  |
| `Order` | number |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `GET lists/getLists` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lists.md) for the provider-specific parameters and requirements.

