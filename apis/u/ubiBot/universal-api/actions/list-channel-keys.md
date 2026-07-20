# UbiBot: List Channel Keys

Retrieves channel API keys from UbiBot.

```
GET https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-channel-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UbiBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-channel-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-channel-keys?${params}`, {
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
| `channelId` | string | no | UbiBot channel identifier from the channel URL or channel list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "read_keys": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "note": "string",
          "read_key": "string",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      ],
      "result": "string",
      "server_time": "2026-05-07T12:00:00.000Z",
      "write_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `read_keys` | array<object> | Read-only keys available for the channel. |
| `read_keys[].created_at` | date | Key creation time. |
| `read_keys[].note` | string | Optional note for the read-only key. |
| `read_keys[].read_key` | string | Read-only API key. |
| `read_keys[].updated_at` | date | Key update time. |
| `result` | string | UbiBot success or error result status. |
| `server_time` | date | UbiBot server timestamp. |
| `write_key` | string | Current channel write key. |

## Native endpoint

Through the native UbiBot API, this operation is `GET /channels/:channelId/api_keys` (base URL `https://webapi.ubibot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-keys.md) for the provider-specific parameters and requirements.

