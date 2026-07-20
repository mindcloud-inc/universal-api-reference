# Streamer.bot: Get Actions

Retrieves all available actions from Streamer.bot.

```
GET https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/get-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamer.bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/get-actions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/get-actions?${params}`, {
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
      "enabled": true,
      "group": "string",
      "id": "string",
      "name": "Ava Chen",
      "subactionCount": 1,
      "triggerCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean | Whether the action is enabled. |
| `group` | string | Streamer.bot action group. |
| `id` | string | Streamer.bot action GUID. |
| `name` | string | Streamer.bot action name. |
| `subactionCount` | number | Number of sub-actions in the Streamer.bot action. |
| `triggerCount` | number | Number of triggers attached to the Streamer.bot action. |

## Native endpoint

Through the native Streamer.bot API, this operation is `GET /GetActions` (base URL `https://allow-freely-princess-carefully.trycloudflare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-actions.md) for the provider-specific parameters and requirements.

