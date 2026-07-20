# UbiBot: Get Channel

Retrieves a channel and its latest sensor data from UbiBot.

```
GET https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UbiBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/get-channel?${params}`, {
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
| `channelId` | string | yes | UbiBot channel identifier from the channel URL or channel list. Example: `12345`. |

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
| `channels` | array<object> | Metadata for the requested channel. |
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

Through the native UbiBot API, this operation is `GET /channels/:channelId` (base URL `https://webapi.ubibot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

