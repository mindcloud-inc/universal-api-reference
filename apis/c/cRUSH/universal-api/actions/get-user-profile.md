# CRUSH: Get User Profile



```
GET https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/get-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRUSH `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/get-user-profile?${params}`, {
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
      "aiCredits": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstLogin": "2026-05-07T12:00:00.000Z",
      "lastLogin": "2026-05-07T12:00:00.000Z",
      "notificationSettings": [
        {}
      ],
      "personalization": {},
      "subscriptions": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiCredits` | object | Current AI credit balances. |
| `createdAt` | date | When the profile row was created. |
| `email` | string | Email address for the user profile. |
| `firstLogin` | date | When the user first logged in. |
| `lastLogin` | date | When the user last logged in. |
| `notificationSettings` | array<object> | Notification preference entries. |
| `personalization` | object | Saved personalization preferences. |
| `subscriptions` | array<object> | Subscription entries for the user. |
| `updatedAt` | date | When the profile row was last updated. |
| `userId` | string | Unique CRUSH user identifier. |

## Native endpoint

Through the native CRUSH API, this operation is `GET /aws/userprofiles` (base URL `https://app.crushthememory.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-profile.md) for the provider-specific parameters and requirements.

