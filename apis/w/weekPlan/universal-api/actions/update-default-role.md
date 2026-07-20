# Week Plan: Update Default Role



```
PUT https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/update-default-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/update-default-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/update-default-role', {
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
      "IsDefault": true,
      "RoleId": 1,
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
| `IsDefault` | boolean |  |
| `RoleId` | number |  |
| `Text` | string |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `PATCH roles/0` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-default-role.md) for the provider-specific parameters and requirements.

