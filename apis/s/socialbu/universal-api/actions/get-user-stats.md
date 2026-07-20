# Socialbu: Get User Stats

Retrieves user stats from SocialBu insights.

```
GET https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-user-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-user-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-user-stats?${params}`, {
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
      "inactiveAccounts": 1,
      "unreadFeeds": 1,
      "userAutomations": 1,
      "userFailedPosts": 1,
      "userPendingPosts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inactiveAccounts` | number |  |
| `unreadFeeds` | number |  |
| `userAutomations` | number |  |
| `userFailedPosts` | number |  |
| `userPendingPosts` | number |  |

## Native endpoint

Through the native Socialbu API, this operation is `GET /insights/stats` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-stats.md) for the provider-specific parameters and requirements.

