# VoiceGenie: Check Call Transfer Status

Retrieves call transfer status from VoiceGenie.

```
GET https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/check-call-transfer-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceGenie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/check-call-transfer-status?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/check-call-transfer-status?${params}`, {
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
| `campaignId` | string | yes | Campaign associated with the transfer. |

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
| `message` | string | Provider message returned for the transfer-status lookup. |
| `success` | boolean | Whether VoiceGenie found transfer status data for the campaign. |

## Native endpoint

Through the native VoiceGenie API, this operation is `POST /publicRestApiActions/checkCallTransferStatus` (base URL `https://core-saas.voicegenie.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-call-transfer-status.md) for the provider-specific parameters and requirements.

