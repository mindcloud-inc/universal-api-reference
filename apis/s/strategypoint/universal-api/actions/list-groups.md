# Strategypoint: List Groups

Retrieves groups from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-groups?${params}`, {
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
      "active": true,
      "dashboardAccess": true,
      "groupId": 1,
      "layoutAccess": {},
      "name": "Ava Chen",
      "sortOrder": 1,
      "templateAccess": {},
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the group is active. |
| `dashboardAccess` | boolean | Whether the group has dashboard access. |
| `groupId` | number | The unique group identifier. |
| `layoutAccess` | object | The group's layout access configuration. |
| `name` | string | The group name. |
| `sortOrder` | number | The sort order for the group. |
| `templateAccess` | object | The group's template access configuration. |
| `users` | array<object> | The users assigned to the group. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /groups` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

