# Splitwise: Get Current User

Retrieves the current user's details from Splitwise.

```
GET https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Splitwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/get-current-user?${params}`, {
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
      "addFriendUrl": "https://example.com",
      "countryCode": "string",
      "customPicture": true,
      "dateFormat": "string",
      "defaultCurrency": "string",
      "defaultGroupId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "forceRefreshAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastName": "Chen",
      "locale": "string",
      "notifications": {},
      "notificationsCount": 1,
      "notificationsRead": "2026-05-07T12:00:00.000Z",
      "picture": {},
      "registrationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addFriendUrl` | string | Invite URL for adding the current user as a friend. |
| `countryCode` | string | Country code for the user. |
| `customPicture` | boolean | Whether the user has a custom profile picture. |
| `dateFormat` | string | Preferred date format for the user. |
| `defaultCurrency` | string | Default currency code for the user. |
| `defaultGroupId` | number | Default group identifier for the user. |
| `email` | string | Primary email address for the user. |
| `firstName` | string | The user's first name. |
| `forceRefreshAt` | date | Provider refresh marker when present. |
| `id` | number | Unique identifier for the current user. |
| `lastName` | string | The user's last name. |
| `locale` | string | Preferred locale for the user. |
| `notifications` | object | Notification preferences for the user. |
| `notificationsCount` | number | Unread notification count. |
| `notificationsRead` | date | Timestamp when notifications were last read. |
| `picture` | object | Profile image URLs in multiple sizes. |
| `registrationStatus` | string | Splitwise registration state for the user. |

## Native endpoint

Through the native Splitwise API, this operation is `GET /get_current_user` (base URL `https://secure.splitwise.com/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

