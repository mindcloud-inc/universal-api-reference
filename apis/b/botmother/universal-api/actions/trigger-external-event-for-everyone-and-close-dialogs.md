# Botmother: Trigger External Event For Everyone And Close Dialogs

Triggers an external event in Botmother for all users and closes chats.

```
POST https://connect.mindcloud.co/v1/universal/botmother/latest/actions/trigger-external-event-for-everyone-and-close-dialogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botmother `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botmother/latest/actions/trigger-external-event-for-everyone-and-close-dialogs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botmother/latest/actions/trigger-external-event-for-everyone-and-close-dialogs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Optional JSON payload copied into last_request. Default: `{}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limits": {
        "exceeded": true,
        "queued": {
          "big": 1,
          "small": 1
        },
        "remained": {
          "big": 1,
          "small": 1
        }
      },
      "payload": [
        [
          {}
        ]
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limits` | object | Botmother queue limit summary returned with the request. |
| `limits.exceeded` | boolean | Whether Botmother reports that queue limits were exceeded. |
| `limits.queued` | object | Number of events queued in each Botmother queue tier. |
| `limits.queued.big` | number | Count queued in the big Botmother processing queue. |
| `limits.queued.small` | number | Count queued in the small Botmother processing queue. |
| `limits.remained` | object | Remaining Botmother queue capacity after this request. |
| `limits.remained.big` | number | Remaining capacity in the big Botmother processing queue. |
| `limits.remained.small` | number | Remaining capacity in the small Botmother processing queue. |
| `payload[]` | array<object> | Queued Botmother external event records returned by the API. |
| `payload[].__v` | number | Botmother internal version number for the queued event record. |
| `payload[]._id` | string | Botmother external event record id. |
| `payload[].createdAt` | string | Timestamp when Botmother created the queued event record. |
| `payload[].errorCount` | number | Number of delivery errors currently recorded for the queued event. |
| `payload[].errorsSet[]` | array<object> | Provider-reported event processing errors, when present. |
| `payload[].partitionsWasCreated` | boolean | Whether Botmother created queue partitions for the event. |
| `payload[].processedCount` | number | Number of deliveries processed so far for the queued event. |
| `payload[].queryOptions` | object | Resolved audience filters used by Botmother for this event. |
| `payload[].queryOptions.botId` | string | Botmother bot id that owns the external event. |
| `payload[].queryOptions.exclusiveTags[]` | array<string> | Excluded Botmother audience tags. |
| `payload[].queryOptions.platformIds[]` | array<string> | Resolved channel-specific platform user ids included in the event audience. |
| `payload[].queryOptions.platforms[]` | array<string> | Target platforms resolved by Botmother. |
| `payload[].queryOptions.storeIds[]` | array<string> | Resolved Botmother user ids included in the event audience. |
| `payload[].queryOptions.tags[]` | array<string> | Included Botmother audience tags. |
| `payload[].sendData` | object | Event delivery payload Botmother will send to the matching users. |
| `payload[].sendData.attachments[]` | array<object> | Attachment objects included in the outgoing event, when present. |
| `payload[].sendData.data` | object | Custom data payload Botmother will place into last_request. |
| `payload[].sendData.formatedMessage` | string | Botmother-formatted message body, when returned by the provider. |
| `payload[].sendData.message` | string | Message body used by the event when the target type sends a message. |
| `payload[].sendData.screen` | string | Target Botmother screen name configured for the event. |
| `payload[].sendData.stopDialog` | boolean | Whether Botmother will close the current dialog before delivering the event. |
| `payload[].sendData.type` | string | Configured Botmother target type for the event, such as screen. |
| `payload[].shard` | string | Botmother internal shard identifier for the queued event. |
| `payload[].status` | string | Current Botmother processing status for the queued event. |
| `payload[].successCount` | number | Number of successful deliveries currently recorded for the queued event. |
| `payload[].totalCount` | number | Total number of matching audience records considered by Botmother. |
| `payload[].type` | string | Botmother record type returned for the queued event. |
| `payload[].updatedAt` | string | Timestamp when Botmother last updated the queued event record. |
| `result` | boolean | True when Botmother accepts the external event request. |

## Native endpoint

Through the native Botmother API, this operation is `POST /` (base URL `{{credentials.eventUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-external-event-for-everyone-and-close-dialogs.md) for the provider-specific parameters and requirements.

