# Week Plan: Reorder Role Actions



```
PUT https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/reorder-role-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/reorder-role-actions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/reorder-role-actions', {
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
      "ActionId": 1,
      "RoleId": 1,
      "RoleOrder": 1,
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
| `RoleId` | number |  |
| `RoleOrder` | number |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `POST actions/roles_reorder` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reorder-role-actions.md) for the provider-specific parameters and requirements.

