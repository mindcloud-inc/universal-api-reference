# Everhour: List Users

Retrieves users from Everhour.

```
GET https://connect.mindcloud.co/v1/universal/everhour/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everhour/latest/actions/list-users?${params}`, {
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
      "avatarUrl": "https://example.com",
      "avatarUrlLarge": "https://example.com",
      "capacity": 1,
      "cost": 1,
      "costHistory": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "enableResourcePlanner": true,
      "favorite": true,
      "groups": [
        {}
      ],
      "headline": "string",
      "id": 1,
      "isEmailVerified": true,
      "name": "Ava Chen",
      "permissions": {},
      "rate": 1,
      "resourcePlannerAccess": {},
      "role": "string",
      "status": "string",
      "timeTrackingPolicy": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `avatarUrlLarge` | string |  |
| `capacity` | number |  |
| `cost` | number |  |
| `costHistory` | array<object> |  |
| `createdAt` | date |  |
| `email` | string |  |
| `enableResourcePlanner` | boolean |  |
| `favorite` | boolean |  |
| `groups` | array<object> |  |
| `headline` | string |  |
| `id` | number |  |
| `isEmailVerified` | boolean |  |
| `name` | string |  |
| `permissions` | object |  |
| `rate` | number |  |
| `resourcePlannerAccess` | object |  |
| `role` | string |  |
| `status` | string |  |
| `timeTrackingPolicy` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Everhour API, this operation is `GET /team/users` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

