# SIGNL4: List Users

Retrieves users from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-users?${params}`, {
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

Through the native SIGNL4 API, this operation is `GET /v2/users` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

