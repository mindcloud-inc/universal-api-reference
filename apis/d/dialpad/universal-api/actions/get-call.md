# Dialpad: Get Call

Retrieves detailed information for a concluded call in Dialpad.

```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-call?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-call?${params}`, {
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
| `id` | number | yes | The call's id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callId": "string",
      "contact": {},
      "dateConnected": 1,
      "dateEnded": 1,
      "dateStarted": 1,
      "direction": "string",
      "duration": 1,
      "externalNumber": "string",
      "internalNumber": "string",
      "isTransferred": true,
      "state": "string",
      "target": {},
      "totalDuration": 1,
      "transcriptionText": "string",
      "wasRecorded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callId` | string | The call ID. |
| `contact` | object | The contact involved in the call. |
| `dateConnected` | number | Timestamp when the call connected. |
| `dateEnded` | number | Timestamp when the call ended. |
| `dateStarted` | number | Timestamp when the call began in Dialpad. |
| `direction` | string | Call direction. |
| `duration` | number | Duration of the call in milliseconds. |
| `externalNumber` | string | The phone number external to the organization. |
| `internalNumber` | string | The phone number internal to the organization. |
| `isTransferred` | boolean | Whether the call was transferred. |
| `state` | string | Current call state. |
| `target` | object | The call target. |
| `totalDuration` | number | Total duration including ring time. |
| `transcriptionText` | string | Text of call transcription when available. |
| `wasRecorded` | boolean | Whether the call was recorded. |

## Native endpoint

Through the native Dialpad API, this operation is `GET /call/:id` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call.md) for the provider-specific parameters and requirements.

