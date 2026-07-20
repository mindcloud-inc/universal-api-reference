# WakaTime: List User Agents

Retrieves a user's WakaTime plugin user agents.

```
GET https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/list-user-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WakaTime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/list-user-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/list-user-agents?${params}`, {
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
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |

## Native endpoint

Through the native WakaTime API, this operation is `GET /users/:user/user_agents` (base URL `https://api.wakatime.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-agents.md) for the provider-specific parameters and requirements.

