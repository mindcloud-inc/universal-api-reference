# SIGNL4: Get User

Retrieves a user from SIGNL4 by ID.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | Identifier of the user to get. Use 'Me' to get information about the currently logged in user. This is not possible with an api key. Can also be an email address of a user in the team or the unique id of an according user object.” |

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
        "dutyMode": 1,
        "lastChange": "2026-05-07T12:00:00.000Z",
        "onDutyTime": 1,
        "overdue": true,
        "teamId": "string",
        "tierId": 1,
        "userId": "string"
      },
      "externalAuthProvider": "string",
      "id": "string",
      "isDeactivated": true,
      "isEnabled": true,
      "isInvite": true,
      "lastSeen": "2026-05-07T12:00:00.000Z",
      "mail": "string",
      "name": "Ava Chen",
      "options": 1,
      "remoteActionPinSet": true,
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
| `dutyInfos` | array<object> |  |
| `dutyInfos.dutyMode` | number |  |
| `dutyInfos.lastChange` | date |  |
| `dutyInfos.onDutyTime` | number |  |
| `dutyInfos.overdue` | boolean |  |
| `dutyInfos.teamId` | string |  |
| `dutyInfos.tierId` | number |  |
| `dutyInfos.userId` | string |  |
| `externalAuthProvider` | string |  |
| `id` | string |  |
| `isDeactivated` | boolean |  |
| `isEnabled` | boolean |  |
| `isInvite` | boolean |  |
| `lastSeen` | date |  |
| `mail` | string |  |
| `name` | string |  |
| `options` | number |  |
| `remoteActionPinSet` | boolean |  |
| `subscriptionId` | string |  |
| `timeZone` | string |  |
| `userImageLastModified` | date |  |
| `webLanguage` | number |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/users/{userId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

