# Everhour: Get Current User

Retrieves the current user from Everhour.

```
GET https://connect.mindcloud.co/v1/universal/everhour/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everhour/latest/actions/get-current-user?${params}`, {
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
      "accounts": [
        {}
      ],
      "activityMode": "string",
      "avatarUrl": "https://example.com",
      "avatarUrlLarge": "https://example.com",
      "capacity": 1,
      "clockOutSettings": {},
      "cost": 1,
      "costHistory": [
        {}
      ],
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateFormat": 1,
      "dateTimeFormat": 1,
      "email": "ava@example.com",
      "enableEmailReminders": true,
      "enableResourcePlanner": true,
      "exportCsvSeparator": 1,
      "exportTimeFormat": 1,
      "favorite": true,
      "groups": [
        {}
      ],
      "hasEmailChangeRequestPending": true,
      "hasPassword": true,
      "headline": "string",
      "id": 1,
      "installStep": "string",
      "isCompany": true,
      "isEmailVerified": true,
      "isSuspended": true,
      "name": "Ava Chen",
      "newsSubscribed": true,
      "notificationSettings": {},
      "nps": true,
      "onboardingVersion": 1,
      "permissions": {},
      "privacyAcceptedAt": "2026-05-07T12:00:00.000Z",
      "rate": 1,
      "resourcePlannerAccess": {},
      "role": "string",
      "screenshoterInstalled": true,
      "signupType": "string",
      "startPage": "string",
      "status": "string",
      "team": {},
      "timeFormat": 1,
      "timeOffPermissions": {},
      "timeRounding": 1,
      "timeRoundingDirection": "string",
      "timeTrackingPolicy": {},
      "timezone": 1,
      "type": "string",
      "webSettings": {},
      "welcomeSeen": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> |  |
| `activityMode` | string |  |
| `avatarUrl` | string |  |
| `avatarUrlLarge` | string |  |
| `capacity` | number |  |
| `clockOutSettings` | object |  |
| `cost` | number |  |
| `costHistory` | array<object> |  |
| `country` | string |  |
| `createdAt` | date |  |
| `dateFormat` | number |  |
| `dateTimeFormat` | number |  |
| `email` | string |  |
| `enableEmailReminders` | boolean |  |
| `enableResourcePlanner` | boolean |  |
| `exportCsvSeparator` | number |  |
| `exportTimeFormat` | number |  |
| `favorite` | boolean |  |
| `groups` | array<object> |  |
| `hasEmailChangeRequestPending` | boolean |  |
| `hasPassword` | boolean |  |
| `headline` | string |  |
| `id` | number |  |
| `installStep` | string |  |
| `isCompany` | boolean |  |
| `isEmailVerified` | boolean |  |
| `isSuspended` | boolean |  |
| `name` | string |  |
| `newsSubscribed` | boolean |  |
| `notificationSettings` | object |  |
| `nps` | boolean |  |
| `onboardingVersion` | number |  |
| `permissions` | object |  |
| `privacyAcceptedAt` | date |  |
| `rate` | number |  |
| `resourcePlannerAccess` | object |  |
| `role` | string |  |
| `screenshoterInstalled` | boolean |  |
| `signupType` | string |  |
| `startPage` | string |  |
| `status` | string |  |
| `team` | object |  |
| `timeFormat` | number |  |
| `timeOffPermissions` | object |  |
| `timeRounding` | number |  |
| `timeRoundingDirection` | string |  |
| `timeTrackingPolicy` | object |  |
| `timezone` | number |  |
| `type` | string |  |
| `webSettings` | object |  |
| `welcomeSeen` | boolean |  |

## Native endpoint

Through the native Everhour API, this operation is `GET /users/me` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

