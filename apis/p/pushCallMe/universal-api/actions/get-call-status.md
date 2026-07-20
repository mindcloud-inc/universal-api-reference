# PushCallMe: Get Call Status

Retrieves call status details from PushCallMe.

```
GET https://connect.mindcloud.co/v1/universal/pushCallMe/latest/actions/get-call-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PushCallMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushCallMe/latest/actions/get-call-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushCallMe/latest/actions/get-call-status?${params}`, {
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
| `requestId` | string | yes | Request identifier returned by the Make Phone Call action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableCalls": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endedAt": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "id": "string",
      "isMissed": true,
      "plan": "string",
      "status": "string",
      "teamId": "string",
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableCalls` | number | Remaining calls available on the current plan. |
| `createdAt` | date | Timestamp when the call was created. |
| `endedAt` | date | Timestamp when the call ended. |
| `from` | string | Caller number used for the call. |
| `id` | string | PushCall call record identifier. |
| `isMissed` | boolean | Whether the call was missed. |
| `plan` | string | Billing plan used for the call. |
| `status` | string | Call outcome such as ANSWERED, BUSY_HERE, TERMINATED, or UNAVAILABLE. |
| `teamId` | string | Team identifier associated with the call. |
| `to` | string | Destination number that was called. |

## Native endpoint

Through the native PushCallMe API, this operation is `GET /api/calls/:requestId` (base URL `https://pushcall.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-status.md) for the provider-specific parameters and requirements.

