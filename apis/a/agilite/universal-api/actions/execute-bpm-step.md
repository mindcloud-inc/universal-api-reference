# Agilite: Execute BPM Step

Executes a BPM record in Agilite.

```
PUT https://connect.mindcloud.co/v1/universal/agilite/latest/actions/execute-bpm-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/execute-bpm-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "processKey": "string",
  "bpmRecordId": "string",
  "optionSelected": "string",
  "currentUser": "string",
  "currentStep": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agilite/latest/actions/execute-bpm-step', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "processKey": "string",
    "bpmRecordId": "string",
    "optionSelected": "string",
    "currentUser": "string",
    "currentStep": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `processKey` | string | yes | Agilit-e BPM process key. |
| `bpmRecordId` | string | yes | BPM record identifier. |
| `optionSelected` | string | yes | Selected BPM step option. |
| `currentUser` | string | yes | User executing the BPM step. |
| `currentStep` | string | yes | Current step key or name for the BPM record. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comments` | string | no | Optional execution comments. |
| `data` | object | no | Optional JSON body sent to the BPM execution endpoint. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agilite API returns.

## Native endpoint

Through the native Agilite API, this operation is `POST /bpm/execute` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-bpm-step.md) for the provider-specific parameters and requirements.

