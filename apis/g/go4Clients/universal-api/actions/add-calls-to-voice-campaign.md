# Go4Clients: Add Calls to Voice Campaign

Adds calls to an existing Go4Clients voice campaign.

```
PUT https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-calls-to-voice-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-calls-to-voice-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceCampaignId": "69dd2799f931660008cdc96f",
  "destinationsList[]": "573004445566"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-calls-to-voice-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceCampaignId": "69dd2799f931660008cdc96f",
    "destinationsList[]": "573004445566"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voiceCampaignId` | string | yes | Voice campaign identifier. Example: `69dd2799f931660008cdc96f`. |
| `destinationsList[]` | array<string> | yes | Destination list of phone numbers. Example: `573004445566`. |
| `stepList[]` | array<object> | no | IVR step list when not using a prebuilt IVR. Example: `[object Object]`. |
| `ivrId` | string | no | Identifier for a prebuilt IVR. Example: `ivr-id`. |
| `customFields` | object | no | Map of personalized IVR fields. Example: `[object Object]`. |
| `priority` | string | no | Priority of the voice calls. Example: `LOW`. |
| `scheduledDate` | string | no | Scheduled date in YYYY-MM-DDTHH:mm:sssZ format. Example: `2026-04-14T10:00:000Z`. |

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
      "sender": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string | Identifier of the voice campaign. |
| `campaignName` | string | Name of the voice campaign. |
| `destinationsList` | array<string> | Destinations included in the request. |
| `generatedIds` | object | Generated IDs mapped to destinations. |
| `ivrId` | string | IVR identifier when used. |
| `priority` | string | Priority of the voice request. |
| `recordCall` | boolean | Whether call recording is enabled. |
| `sender` | string | Sender used for the campaign. |

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/campaigns/voice/v1.0/{{voice_campaign_id}}` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-calls-to-voice-campaign.md) for the provider-specific parameters and requirements.

