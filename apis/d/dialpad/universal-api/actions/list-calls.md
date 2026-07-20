# Dialpad: List Calls

Retrieves concluded call records from Dialpad.

```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-calls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-calls?${params}`, {
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
| `cursor` | string | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |
| `include_anonymized` | boolean | no | If set to true, includes call records that have been anonymized. |
| `started_after` | number | no | Only includes calls that started more recently than the specified UTC millisecond timestamp. |
| `started_before` | number | no | Only includes calls that started prior to the specified UTC millisecond timestamp. |
| `target_id` | number | no | The ID of a target to filter against. |
| `target_type` | string | no | The target type associated with the target ID. |

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

Through the native Dialpad API, this operation is `GET /call` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calls.md) for the provider-specific parameters and requirements.

