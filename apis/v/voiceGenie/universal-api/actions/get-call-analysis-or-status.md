# VoiceGenie: Get Call Analysis or Status

Retrieves call analysis or status from VoiceGenie.

```
GET https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/get-call-analysis-or-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceGenie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/get-call-analysis-or-status?connectionId=$CONNECTION_ID&campaignId=string&customerNumber=string&action=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string",
  "customerNumber": "string",
  "action": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/get-call-analysis-or-status?${params}`, {
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
| `campaignId` | string | yes | Campaign associated with the call. |
| `customerNumber` | string | yes | Customer number used in the campaign, preferably in E.164 format. |
| `action` | string | yes | Use `analysis` for transcripts or `status` for the latest call state. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native VoiceGenie API returns.

## Native endpoint

Through the native VoiceGenie API, this operation is `POST /publicRestApiActions/callAnalysisOrStatus` (base URL `https://core-saas.voicegenie.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-analysis-or-status.md) for the provider-specific parameters and requirements.

