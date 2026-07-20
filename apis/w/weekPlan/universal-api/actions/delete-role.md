# Week Plan: Delete Role



```
DELETE https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-role?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-role?${params}`, {
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
      "DeletedAt": "string",
      "IsDeleted": true,
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
| `DeletedAt` | string |  |
| `IsDeleted` | boolean |  |
| `RoleId` | number |  |
| `Text` | string |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `PATCH roles/:roleId` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-role.md) for the provider-specific parameters and requirements.

