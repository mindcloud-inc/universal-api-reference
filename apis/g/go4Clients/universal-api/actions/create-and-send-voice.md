# Go4Clients: Create and Send Voice

Creates a campaign and sends voice calls in Go4Clients.

```
POST https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-and-send-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-and-send-voice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationsList[]": "573004445566",
  "sender": "573112233445",
  "campaignName": "MindCloud voice blast"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-and-send-voice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationsList[]": "573004445566",
    "sender": "573112233445",
    "campaignName": "MindCloud voice blast"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destinationsList[]` | array<string> | yes | Destination phone numbers in international format. Example: `573004445566`. |
| `stepList[]` | array<object> | no | Step list for the IVR flow when not using a prebuilt IVR. Example: `[object Object]`. |
| `ivrId` | string | no | Identifier for a prebuilt IVR. Example: `ivr-id`. |
| `customFields` | object | no | Map of values used to personalize the IVR. Example: `[object Object]`. |
| `sender` | string | yes | Caller ID shown to recipients. Example: `573112233445`. |
| `priority` | string | no | Priority of the calls in Go4Clients. Example: `LOW`. |
| `scheduledDate` | string | no | Scheduled date in YYYY-MM-DDTHH:mm:sssZ format. Example: `2026-04-14T10:00:000Z`. |
| `campaignName` | string | yes | Campaign name to identify the call in analytics. Example: `MindCloud voice blast`. |
| `text2speech` | string | no | Text that will be converted into voice for the call. Example: `Hello from MindCloud`. |
| `voice` | string | no | Voice used to convert text to speech. Example: `PEDRO`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "campaignName": "Ava Chen",
      "destinationsList": [
        "string"
      ],
      "generatedIds": {},
      "ivrId": "string",
      "priority": "string",
      "recordCall": true,
      "sender": "string",
      "text2speech": "string",
      "voice": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string | Identifier of the created voice campaign. |
| `campaignName` | string | Name of the created voice campaign. |
| `destinationsList` | array<string> | Destinations included in the request. |
| `generatedIds` | object | Generated IDs mapped to destinations. |
| `ivrId` | string | IVR identifier when used. |
| `priority` | string | Priority of the voice campaign. |
| `recordCall` | boolean | Whether call recording is enabled. |
| `sender` | string | Sender used for the voice campaign. |
| `text2speech` | string | Text-to-speech message when used. |
| `voice` | string | Voice used for text-to-speech. |

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/campaigns/voice/v2.0/event` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-and-send-voice.md) for the provider-specific parameters and requirements.

