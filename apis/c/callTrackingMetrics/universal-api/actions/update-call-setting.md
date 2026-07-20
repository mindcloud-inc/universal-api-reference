# CallTrackingMetrics: Update Call Setting

Updates an existing call setting in CallTrackingMetrics.

```
PUT https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/update-call-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/update-call-setting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "callSettingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/update-call-setting', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "callSettingId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callSettingId` | string | yes | The CallTrackingMetrics call setting ID. |
| `description` | string | no | An updated description for the call setting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "calleridEnabled": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": true,
      "description": "string",
      "id": "string",
      "inboundRecordingsOn": true,
      "name": "Ava Chen",
      "outboundRecordingOn": true,
      "playMessage": "string",
      "spamBlocking": true,
      "transcription": true,
      "updateAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `calleridEnabled` | boolean |  |
| `createdAt` | date |  |
| `default` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `inboundRecordingsOn` | boolean |  |
| `name` | string |  |
| `outboundRecordingOn` | boolean |  |
| `playMessage` | string |  |
| `spamBlocking` | boolean |  |
| `transcription` | boolean |  |
| `updateAt` | date |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `PUT /accounts/:accountId/call_settings/:callSettingId.json` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-call-setting.md) for the provider-specific parameters and requirements.

