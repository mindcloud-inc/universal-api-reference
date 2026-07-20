# Ringg AI: Initiate Individual Call

Initiates an individual outbound call in Ringg AI.

```
POST https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/initiate-individual-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/initiate-individual-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "mobileNumber": "string",
  "agentId": "string",
  "fromNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/initiate-individual-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "mobileNumber": "string",
    "agentId": "string",
    "fromNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the person to call |
| `mobileNumber` | string | yes | The phone number to call (must include country code, e.g., +91 for India) |
| `agentId` | string | yes | UUID of the agent that will handle the call |
| `fromNumber` | string | yes | The phone number to call from (with country code) |
| `customArgsValues` | object | no | Custom variables that will be replaced in the agent's prompt using @{{variable_name}} syntax |
| `customArgsValues.companyName` | string | no | Company name for context |
| `customArgsValues.appointmentDate` | string | no | Appointment date |
| `customArgsValues.productName` | string | no | Product name for sales calls |
| `smartFormatter` | object | no | (Optional) Smart formatting for callee name — supports first name extraction and dictionary-based transliteration |
| `smartFormatter.extractFirstName` | boolean | no | Extract the first actual name from the full name, skipping common prefixes (Mr, Mrs, Dr, etc.) |
| `smartFormatter.transliteration` | boolean | no | Transliterate the extracted name to the target language using a local dictionary. When enabled, extract_first_name is automatically applied. |
| `smartFormatter.transliterationLanguage` | object | no | Language configuration for transliteration |
| `smartFormatter.transliterationLanguage.source` | string | no | Source language code (default: en) |
| `smartFormatter.transliterationLanguage.target` | string | no | Target language code (default: hi) |
| `callConfig` | object | no | (Optional) Override default call configuration |
| `callConfig.idleTimeoutWarning` | number | no | Seconds before idle warning (default: 5) |
| `callConfig.idleTimeoutEnd` | number | no | Seconds before call termination (default: 10) |
| `callConfig.maxCallLength` | number | no | Maximum call duration in seconds (default: 240) |
| `callConfig.callRetryConfig` | object | no | Retry configuration for failed calls |
| `callConfig.callRetryConfig.retryCount` | number | no | Number of retry attempts |
| `callConfig.callRetryConfig.retryBusy` | number | no | Minutes to wait if busy (default: 30) |
| `callConfig.callRetryConfig.retryNotPicked` | number | no | Minutes to wait if not picked (default: 30) |
| `callConfig.callRetryConfig.retryFailed` | number | no | Minutes to wait if failed (default: 30) |
| `callConfig.callTime` | object | no | Time window configuration for calls |
| `callConfig.callTime.callStartTime` | string | no | When calls can start (default: 00:00) |
| `callConfig.callTime.callEndTime` | string | no | When calls must end (default: 23:00) |
| `callConfig.callTime.timezone` | string | no | Timezone for call times (default: Asia/Kolkata) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "agentId": "string",
        "callDirection": "string",
        "callId": "string",
        "callStatus": "string",
        "customArgsValues": {},
        "initiatedAt": "2026-05-07T12:00:00.000Z"
      },
      "message": "string",
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
| `data.agentId` | string |  |
| `data.callDirection` | string |  |
| `data.callId` | string |  |
| `data.callStatus` | string | The current status of the call |
| `data.customArgsValues` | object | Custom variables passed in the request |
| `data.initiatedAt` | date |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `POST /calling/outbound/individual` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initiate-individual-call.md) for the provider-specific parameters and requirements.

