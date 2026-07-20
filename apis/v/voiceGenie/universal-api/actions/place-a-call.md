# VoiceGenie: Place a Call

Creates a new call in VoiceGenie.

```
POST https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/place-a-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceGenie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/place-a-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "customerNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/place-a-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "customerNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | Recurring campaign ID that should receive the call. |
| `customerNumber` | string | yes | Customer number in E.164 format with a leading + and no spaces or punctuation. |
| `customerInformation` | object | no | Optional object of string values used for dynamic variables such as first_name and last_name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message returned for the place-call request. |
| `success` | boolean | Whether VoiceGenie accepted the place-call request. |

## Native endpoint

Through the native VoiceGenie API, this operation is `POST /publicRestApiActions/placeCall` (base URL `https://core-saas.voicegenie.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/place-a-call.md) for the provider-specific parameters and requirements.

