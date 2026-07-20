# Week Plan: Update List



```
PUT https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/update-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/update-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/update-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native Week Plan API, this operation is `PATCH lists/:listId` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list.md) for the provider-specific parameters and requirements.

