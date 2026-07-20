# Socialbu: Get Team Activity

Retrieves team activity logs from SocialBu insights.

```
GET https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-team-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-team-activity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-team-activity?${params}`, {
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
      "action": "string",
      "created_at": "string",
      "id": 1,
      "items": [
        {}
      ],
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `created_at` | string |  |
| `id` | number |  |
| `items` | array<object> |  |
| `user` | object |  |

## Native endpoint

Through the native Socialbu API, this operation is `GET /insights/teams/activity` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-activity.md) for the provider-specific parameters and requirements.

