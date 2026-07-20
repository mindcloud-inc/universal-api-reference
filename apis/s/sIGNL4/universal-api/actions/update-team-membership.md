# SIGNL4: Update Team Membership

Updates a team membership in SIGNL4.

```
PUT https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/update-team-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/update-team-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/update-team-membership', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Team the user you want to update belongs to at the moment. |
| `userId` | string | yes | User ID of user you want to update. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requesterUserId` | string | no | User ID of user which you want to change role with. This must be provided when using an api key. This user must have role administrator (for setting administrator role) or team administrator (for setting rights. |
| `setUserOnDuty` | boolean | no | Sets new duty status for user if user is moved to a different team. User is on duty be default. Default: `true`. |
| `teamId` | string | no |  |
| `roleId` | string | no |  |
| `isValid` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "colorIndex": 1,
      "contactAddresses": [
        {}
      ],
      "dutyInfos": {
        "lastChange": "2026-05-07T12:00:00.000Z",
        "onDuty": true,
        "onManagerDuty": true,
        "overdue": true,
        "teamId": "string",
        "userId": "string"
      },
      "externalAuthProvider": "string",
      "id": "string",
      "isDeactivated": true,
      "isEnabled": true,
      "isInvite": true,
      "isRemoteActionPinSet": true,
      "lastSeen": "2026-05-07T12:00:00.000Z",
      "mail": "string",
      "name": "Ava Chen",
      "options": 1,
      "roleId": "string",
      "subscriptionId": "string",
      "timeZone": "string",
      "userImageLastModified": "2026-05-07T12:00:00.000Z",
      "webLanguage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colorIndex` | number |  |
| `contactAddresses` | array<object> |  |
| `dutyInfos` | object |  |
| `dutyInfos.lastChange` | date |  |
| `dutyInfos.onDuty` | boolean |  |
| `dutyInfos.onManagerDuty` | boolean |  |
| `dutyInfos.overdue` | boolean |  |
| `dutyInfos.teamId` | string |  |
| `dutyInfos.userId` | string |  |
| `externalAuthProvider` | string |  |
| `id` | string |  |
| `isDeactivated` | boolean |  |
| `isEnabled` | boolean |  |
| `isInvite` | boolean |  |
| `isRemoteActionPinSet` | boolean |  |
| `lastSeen` | date |  |
| `mail` | string |  |
| `name` | string |  |
| `options` | number |  |
| `roleId` | string |  |
| `subscriptionId` | string |  |
| `timeZone` | string |  |
| `userImageLastModified` | date |  |
| `webLanguage` | number |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `PUT /v2/teams/{teamId}/memberships/{userId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team-membership.md) for the provider-specific parameters and requirements.

