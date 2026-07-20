# Ringg AI: Get Call Details

Retrieves call details from Ringg AI.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-call-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-call-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-call-details?${params}`, {
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
| `id` | string | yes | (Required) The unique identifier (UUID) of the call. |
| `sendAnalysis` | boolean | no | (Optional) Whether to include analysis data (platform_analysis and client_analysis) in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "agentId": "string",
        "callDirection": "string",
        "calleeName": "Ava Chen",
        "callStatus": "string",
        "callSubStatus": "string",
        "clientAnalysis": {},
        "fromNumber": "string",
        "id": "string",
        "initiationTime": "2026-05-07T12:00:00.000Z",
        "platformAnalysis": {},
        "recordingUrl": "https://example.com",
        "toNumber": "string",
        "transcriptionUrl": [
          {
            "bot": "https://example.com",
            "user": "https://example.com"
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.agentId` | string | The ID of the agent that handled the call |
| `data.callDirection` | string | The direction of the call |
| `data.calleeName` | string | The name of the person called |
| `data.callStatus` | string | The current status of the call |
| `data.callSubStatus` | string | The sub-status of the call providing more detail on the call outcome |
| `data.clientAnalysis` | object | Client-specific analysis of the call (only included when send_analysis=true) |
| `data.fromNumber` | string | The phone number the call was made from |
| `data.id` | string | The unique identifier of the call |
| `data.initiationTime` | date | When the call was initiated |
| `data.platformAnalysis` | object | Platform-generated analysis of the call (only included when send_analysis=true) |
| `data.recordingUrl` | string | URL to the call recording |
| `data.toNumber` | string | The phone number the call was made to |
| `data.transcriptionUrl` | array<object> | Array of conversation turns between bot and user |
| `data.transcriptionUrl[].bot` | string | Bot's message |
| `data.transcriptionUrl[].user` | string | User's message |
| `status` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /calling/call-details` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-details.md) for the provider-specific parameters and requirements.

