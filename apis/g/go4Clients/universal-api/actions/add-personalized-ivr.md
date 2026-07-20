# Go4Clients: Add Personalized IVR

Adds a personalized IVR to a Go4Clients voice campaign.

```
PUT https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-personalized-ivr
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-personalized-ivr" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceCampaignId": "69dd2799f931660008cdc96f",
  "destinationsList[]": "57312145698"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-personalized-ivr', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceCampaignId": "69dd2799f931660008cdc96f",
    "destinationsList[]": "57312145698"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voiceCampaignId` | string | yes | Voice campaign identifier. Example: `69dd2799f931660008cdc96f`. |
| `destinationsList[]` | array<string> | yes | Destination list of phone numbers. Example: `57312145698`. |
| `ivrId` | string | no | Identifier of the IVR to use in the call. Example: `5c8bf92ca73e1a0007e25851`. |
| `customFields` | object | no | Map of values used to personalize the IVR. Example: `[object Object]`. |
| `stepList[]` | array<object> | no | Optional IVR step list when no IVR ID is provided. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Go4Clients API returns.

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/campaigns/voice/v1.0/{{voice_campaign_id}}` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-personalized-ivr.md) for the provider-specific parameters and requirements.

