# JustCall: Update a Call

Updates an existing call in JustCall.

```
PUT https://connect.mindcloud.co/v1/universal/justCall/latest/actions/update-a-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/update-a-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/justCall/latest/actions/update-a-call', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The JustCall call ID or SID. |
| `notes` | string | no | Updated notes for the completed call. |

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

Through the native JustCall API, this operation is `PUT /v2.1/calls/:id` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-call.md) for the provider-specific parameters and requirements.

