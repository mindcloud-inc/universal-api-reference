# Everhour Universal API Examples

These examples use the MindCloud API key and Everhour connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Everhour.

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

Example response:

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

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/everhour/latest/actions/get-current-user).

## Add Time

Creates a new time record in Everhour.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/add-time" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "time": 1,
  "date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everhour/latest/actions/add-time', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "time": 1,
    "date": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "cost": 1,
      "costRate": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "history": [
        {}
      ],
      "id": 1,
      "isLocked": true,
      "lastHistory": {},
      "lockReasons": [
        {}
      ],
      "manualTime": 1,
      "pastDateTime": 1,
      "task": {},
      "time": 1,
      "timerTime": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Time action reference](actions/add-time.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/everhour/latest/actions/add-time).
