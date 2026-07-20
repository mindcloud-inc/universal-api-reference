# VoiceGenie: Get Inbound Call Updates

Retrieves inbound call updates from VoiceGenie.

```
GET https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/get-inbound-call-updates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceGenie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/get-inbound-call-updates?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/get-inbound-call-updates?${params}`, {
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
| `campaignId` | string | yes | Campaign tied to the inbound number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native VoiceGenie API returns.

## Native endpoint

Through the native VoiceGenie API, this operation is `POST /publicRestApiActions/inboundCallUpdate` (base URL `https://core-saas.voicegenie.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbound-call-updates.md) for the provider-specific parameters and requirements.

