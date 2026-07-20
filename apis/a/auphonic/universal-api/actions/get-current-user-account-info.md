# Auphonic: Get Current User Account Info

Retrieves current user account info from Auphonic.

```
GET https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-current-user-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auphonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-current-user-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-current-user-account-info?${params}`, {
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
      "credits": 1,
      "dateJoined": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "errorEmail": true,
      "lowCreditsEmail": true,
      "lowCreditsThreshold": 1,
      "notificationEmail": true,
      "onetimeCredits": 1,
      "rechargeDate": "2026-05-07T12:00:00.000Z",
      "rechargeRecurringCredits": 1,
      "recurringCredits": 1,
      "userId": "string",
      "username": "Ava Chen",
      "warningEmail": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number |  |
| `dateJoined` | date |  |
| `email` | string |  |
| `errorEmail` | boolean |  |
| `lowCreditsEmail` | boolean |  |
| `lowCreditsThreshold` | number |  |
| `notificationEmail` | boolean |  |
| `onetimeCredits` | number |  |
| `rechargeDate` | date |  |
| `rechargeRecurringCredits` | number |  |
| `recurringCredits` | number |  |
| `userId` | string |  |
| `username` | string |  |
| `warningEmail` | boolean |  |

## Native endpoint

Through the native Auphonic API, this operation is `GET /user.json` (base URL `https://auphonic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-account-info.md) for the provider-specific parameters and requirements.

