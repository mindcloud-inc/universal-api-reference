# Streak: Get Current User

Retrieves the current user from Streak.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-current-user?${params}`, {
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
      "canceledTrial": true,
      "creationTimestamp": 1,
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstExtension": "string",
      "firstOauthTimestamp": 1,
      "googleAnalyticsClientId": "string",
      "googleProfileFirstName": "Ava",
      "googleProfileFullName": "Ava Chen",
      "googleProfileGender": "string",
      "googleProfileId": "string",
      "googleProfileLastName": "Chen",
      "googleProfileLink": "https://example.com",
      "googleProfileLocale": "string",
      "googleProfilePhotoUrl": "https://example.com",
      "hasCancellationDiscount": true,
      "intercomHmac": "string",
      "isOauthComplete": true,
      "key": "string",
      "lastProPlusTrialStart": 1,
      "lastSavedTimestamp": 1,
      "lastSeenTimestamp": 1,
      "lastTrialLength": 1,
      "lastTrialStart": 1,
      "lastUpdatedTimestamp": 1,
      "onTrialWithoutCreditCard": true,
      "orgKey": "string",
      "timezoneId": "string",
      "tourId": "string",
      "usedPlatforms": [
        {}
      ],
      "userKey": "string",
      "userSettingsKey": "string",
      "userSource": "string",
      "wantsTaskDigestEmail": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canceledTrial` | boolean |  |
| `creationTimestamp` | number |  |
| `displayName` | string |  |
| `email` | string |  |
| `firstExtension` | string |  |
| `firstOauthTimestamp` | number |  |
| `googleAnalyticsClientId` | string |  |
| `googleProfileFirstName` | string |  |
| `googleProfileFullName` | string |  |
| `googleProfileGender` | string |  |
| `googleProfileId` | string |  |
| `googleProfileLastName` | string |  |
| `googleProfileLink` | string |  |
| `googleProfileLocale` | string |  |
| `googleProfilePhotoUrl` | string |  |
| `hasCancellationDiscount` | boolean |  |
| `intercomHmac` | string |  |
| `isOauthComplete` | boolean |  |
| `key` | string |  |
| `lastProPlusTrialStart` | number |  |
| `lastSavedTimestamp` | number |  |
| `lastSeenTimestamp` | number |  |
| `lastTrialLength` | number |  |
| `lastTrialStart` | number |  |
| `lastUpdatedTimestamp` | number |  |
| `onTrialWithoutCreditCard` | boolean |  |
| `orgKey` | string |  |
| `timezoneId` | string |  |
| `tourId` | string |  |
| `usedPlatforms` | array<object> |  |
| `userKey` | string |  |
| `userSettingsKey` | string |  |
| `userSource` | string |  |
| `wantsTaskDigestEmail` | boolean |  |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v1/users/me` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

