# HoneyHive: Get Session

Retrieves an existing session from HoneyHive.

```
GET https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-session?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/get-session?${params}`, {
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
| `sessionId` | string | yes | Session ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "childrenIds": [
        "string"
      ],
      "config": {},
      "duration": 1,
      "endTime": 1,
      "error": "string",
      "eventId": "string",
      "eventName": "Ava Chen",
      "eventType": "string",
      "feedback": {},
      "inputs": {},
      "metadata": {},
      "metrics": {},
      "outputs": {},
      "parentId": "string",
      "projectId": "string",
      "sessionId": "string",
      "source": "string",
      "startTime": 1,
      "userProperties": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `childrenIds` | array<string> |  |
| `config` | object |  |
| `duration` | number |  |
| `endTime` | number |  |
| `error` | string |  |
| `eventId` | string |  |
| `eventName` | string |  |
| `eventType` | string |  |
| `feedback` | object |  |
| `inputs` | object |  |
| `metadata` | object |  |
| `metrics` | object |  |
| `outputs` | object |  |
| `parentId` | string |  |
| `projectId` | string |  |
| `sessionId` | string |  |
| `source` | string |  |
| `startTime` | number |  |
| `userProperties` | object |  |

## Native endpoint

Through the native HoneyHive API, this operation is `GET /session/{session_id}` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session.md) for the provider-specific parameters and requirements.

