# Harvest: Retrieve Current User

Retrieves the current user from Harvest.

```
GET https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-current-user?${params}`, {
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
      "accessRoles": [
        "string"
      ],
      "avatarUrl": "https://example.com",
      "calendarIntegrationEnabled": true,
      "calendarIntegrationSource": "string",
      "canCreateProjects": true,
      "costRate": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultHourlyRate": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasAccessToAllFutureProjects": true,
      "id": 1,
      "isActive": true,
      "isContractor": true,
      "lastName": "Chen",
      "permissionsClaims": [
        "string"
      ],
      "roles": [
        "string"
      ],
      "telephone": "string",
      "timezone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "weeklyCapacity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessRoles` | array<string> |  |
| `avatarUrl` | string |  |
| `calendarIntegrationEnabled` | boolean |  |
| `calendarIntegrationSource` | string |  |
| `canCreateProjects` | boolean |  |
| `costRate` | number |  |
| `createdAt` | date |  |
| `defaultHourlyRate` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `hasAccessToAllFutureProjects` | boolean |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isContractor` | boolean |  |
| `lastName` | string |  |
| `permissionsClaims` | array<string> |  |
| `roles` | array<string> |  |
| `telephone` | string |  |
| `timezone` | string |  |
| `updatedAt` | date |  |
| `weeklyCapacity` | number |  |

## Native endpoint

Through the native Harvest API, this operation is `GET /v2/users/me` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-current-user.md) for the provider-specific parameters and requirements.

