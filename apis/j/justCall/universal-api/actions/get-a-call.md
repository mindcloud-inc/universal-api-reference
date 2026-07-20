# JustCall: Get a Call

Retrieves a call from JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-call?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-call?${params}`, {
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
| `id` | string | yes | The JustCall call ID or SID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentActive": "string",
      "agentEmail": "ava@example.com",
      "agentId": 1,
      "agentName": "Ava Chen",
      "callDate": "string",
      "callDuration": {},
      "callInfo": {},
      "callSid": "string",
      "callTime": "string",
      "callUserDate": "string",
      "callUserTime": "string",
      "contactEmail": "ava@example.com",
      "contactName": "Ava Chen",
      "contactNumber": "string",
      "costIncurred": 1,
      "id": 1,
      "ivrInfo": {},
      "justcallLineName": "Ava Chen",
      "justcallNumber": "string",
      "queue": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentActive` | string |  |
| `agentEmail` | string |  |
| `agentId` | number |  |
| `agentName` | string |  |
| `callDate` | string |  |
| `callDuration` | object |  |
| `callInfo` | object |  |
| `callSid` | string |  |
| `callTime` | string |  |
| `callUserDate` | string |  |
| `callUserTime` | string |  |
| `contactEmail` | string |  |
| `contactName` | string |  |
| `contactNumber` | string |  |
| `costIncurred` | number |  |
| `id` | number |  |
| `ivrInfo` | object |  |
| `justcallLineName` | string |  |
| `justcallNumber` | string |  |
| `queue` | object |  |

## Native endpoint

Through the native JustCall API, this operation is `GET /v2.1/calls/:id` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-call.md) for the provider-specific parameters and requirements.

