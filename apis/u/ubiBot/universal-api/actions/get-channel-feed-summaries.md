# UbiBot: Get Channel Feed Summaries

Retrieves channel feed summaries from UbiBot.

```
GET https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/get-channel-feed-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UbiBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/get-channel-feed-summaries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/get-channel-feed-summaries?${params}`, {
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
      "channel": {
        "channel_id": "string",
        "name": "Ava Chen"
      },
      "end": "2026-05-07T12:00:00.000Z",
      "feeds": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "field1": {
            "avg": 1,
            "count": 1,
            "max": 1,
            "min": 1
          }
        }
      ],
      "is_truncated": true,
      "num_records": 1,
      "result": "string",
      "results": 1,
      "server_time": "2026-05-07T12:00:00.000Z",
      "start": "2026-05-07T12:00:00.000Z",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | object | Channel metadata for the summaries. |
| `channel.channel_id` | string | Channel identifier. |
| `channel.name` | string | Channel name. |
| `end` | date | Summary end timestamp. |
| `feeds` | array<object> | Hourly feed summary records. |
| `feeds[].created_at` | date | Summary bucket timestamp. |
| `feeds[].field1` | object | Summary statistics for field1. |
| `feeds[].field1.avg` | number | Average field value. |
| `feeds[].field1.count` | number | Number of readings. |
| `feeds[].field1.max` | number | Maximum field value. |
| `feeds[].field1.min` | number | Minimum field value. |
| `is_truncated` | boolean | Whether the summary result was truncated. |
| `num_records` | number | Number of records returned. |
| `result` | string | UbiBot success or error result status. |
| `results` | number | Requested or returned result count. |
| `server_time` | date | UbiBot server timestamp. |
| `start` | date | Summary start timestamp. |
| `timezone` | string | Timezone used for summary grouping. |

## Native endpoint

Through the native UbiBot API, this operation is `GET /channels/:channelId/summary.json` (base URL `https://webapi.ubibot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-feed-summaries.md) for the provider-specific parameters and requirements.

