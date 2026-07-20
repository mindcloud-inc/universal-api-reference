# Instabot: List Recently Updated Users

Finds users in Instabot by update time.

```
GET https://connect.mindcloud.co/v1/universal/instabot/latest/actions/list-recently-updated-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instabot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instabot/latest/actions/list-recently-updated-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instabot/latest/actions/list-recently-updated-users?${params}`, {
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
| `since` | date | no | Return only users updated since this datetime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "developmentCompany": {
        "objectId": 1
      },
      "email": "ava@example.com",
      "friendlyName": "Ava Chen",
      "isDefaultFriendlyName": true,
      "isTestUser": true,
      "lastActivityDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "objectId": 1,
      "rowVersion": 1,
      "status": "string",
      "updateDate": "2026-05-07T12:00:00.000Z",
      "username": "Ava Chen",
      "userType": "string",
      "visitCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createDate` | date |  |
| `description` | string |  |
| `developmentCompany.objectId` | number |  |
| `email` | string |  |
| `friendlyName` | string |  |
| `isDefaultFriendlyName` | boolean |  |
| `isTestUser` | boolean |  |
| `lastActivityDate` | date |  |
| `name` | string |  |
| `objectId` | number |  |
| `rowVersion` | number |  |
| `status` | string |  |
| `updateDate` | date |  |
| `username` | string |  |
| `userType` | string |  |
| `visitCount` | number |  |

## Native endpoint

Through the native Instabot API, this operation is `GET /users/lastUpdated` (base URL `https://api.instabot.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recently-updated-users.md) for the provider-specific parameters and requirements.

