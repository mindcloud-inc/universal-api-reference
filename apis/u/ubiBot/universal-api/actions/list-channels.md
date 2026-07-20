# UbiBot: List Channels

Retrieves available channels from UbiBot.

```
GET https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UbiBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-channels?${params}`, {
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
      "channels": [
        {
          "channel_id": "string",
          "field1": "string",
          "field2": "string",
          "field3": "string",
          "last_entry_date": "2026-05-07T12:00:00.000Z",
          "last_values": "string",
          "name": "Ava Chen",
          "net": "string",
          "public_flag": "string",
          "usage": "string"
        }
      ],
      "result": "string",
      "server_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | array<object> | Channels associated with the account. |
| `channels[].channel_id` | string | Channel identifier. |
| `channels[].field1` | string | Sensor field name. |
| `channels[].field2` | string | Sensor field name. |
| `channels[].field3` | string | Sensor field name. |
| `channels[].last_entry_date` | date | Last sync time. |
| `channels[].last_values` | string | Last sensor values encoded by UbiBot. |
| `channels[].name` | string | Channel name. |
| `channels[].net` | string | Connection state code. |
| `channels[].public_flag` | string | Device public permission flag. |
| `channels[].usage` | string | Device used storage. |
| `result` | string | UbiBot success or error result status. |
| `server_time` | date | UbiBot server timestamp. |

## Native endpoint

Through the native UbiBot API, this operation is `GET /channels` (base URL `https://webapi.ubibot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

