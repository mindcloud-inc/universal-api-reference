# BuildChatbot: Logout

Deletes the current session from BuildChatbot.

```
DELETE https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/logout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildChatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/logout?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/logout?${params}`, {
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
      "data": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Logout result message. |
| `status` | string | Provider response status. |

## Native endpoint

Through the native BuildChatbot API, this operation is `POST /logout` (base URL `https://api.buildchatbot.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/logout.md) for the provider-specific parameters and requirements.

