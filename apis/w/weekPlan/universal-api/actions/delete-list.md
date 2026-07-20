# Week Plan: Delete List



```
DELETE https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-list?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
      "DeletedAt": "string",
      "IsDeleted": true,
      "Name": "Ava Chen",
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
| `DeletedAt` | string |  |
| `IsDeleted` | boolean |  |
| `Name` | string |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `PATCH lists/:listId` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-list.md) for the provider-specific parameters and requirements.

