# Voiceflow: Get Transcript

Retrieves a transcript and its results from Voiceflow.

```
GET https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-transcript?connectionId=$CONNECTION_ID&transcriptId=transcript_1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptId": "transcript_1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-transcript?${params}`, {
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
| `transcriptId` | string | yes | ID of the transcript to target. Example: `transcript_1234567890`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `unredacted` | boolean | no | Return un-redacted logs when available. Example: `false`. |
| `filterConversation` | boolean | no | Only include conversation trace types. Example: `true`. |
| `customTraceTypes[]` | array<string> | no | Additional trace types to include when filterConversation is enabled. Example: `action`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "transcript": {
        "createdAt": "string",
        "endedAt": "string",
        "environmentID": "string",
        "evaluations": [
          {
            "cost": 1,
            "createdAt": "string",
            "default": true,
            "description": "string",
            "id": "string",
            "name": "Ava Chen",
            "reason": "string",
            "type": "string",
            "updatedAt": "string",
            "value": "string"
          }
        ],
        "expiresAt": "string",
        "history": [
          {
            "createdAt": "string",
            "id": "string"
          }
        ],
        "id": "string",
        "interactionCount": 1,
        "logs": [
          {
            "createdAt": "string",
            "data": {
              "payload": "string",
              "type": "string"
            },
            "type": "string",
            "updatedAt": "string"
          }
        ],
        "projectEnvironmentID": {},
        "projectID": "string",
        "properties": [
          {
            "createdAt": "string",
            "default": true,
            "id": "string",
            "metadata": {},
            "name": "Ava Chen",
            "type": "string",
            "updatedAt": "string",
            "value": "string"
          }
        ],
        "recordingURL": {},
        "sessionID": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `transcript.createdAt` | string |  |
| `transcript.endedAt` | string |  |
| `transcript.environmentID` | string |  |
| `transcript.evaluations[].cost` | number |  |
| `transcript.evaluations[].createdAt` | string |  |
| `transcript.evaluations[].default` | boolean |  |
| `transcript.evaluations[].description` | string |  |
| `transcript.evaluations[].id` | string |  |
| `transcript.evaluations[].name` | string |  |
| `transcript.evaluations[].reason` | string |  |
| `transcript.evaluations[].type` | string |  |
| `transcript.evaluations[].updatedAt` | string |  |
| `transcript.evaluations[].value` | string |  |
| `transcript.expiresAt` | string |  |
| `transcript.history[].createdAt` | string |  |
| `transcript.history[].id` | string |  |
| `transcript.id` | string |  |
| `transcript.interactionCount` | number |  |
| `transcript.logs[].createdAt` | string |  |
| `transcript.logs[].data.payload` | string |  |
| `transcript.logs[].data.type` | string |  |
| `transcript.logs[].type` | string |  |
| `transcript.logs[].updatedAt` | string |  |
| `transcript.projectEnvironmentID` | object |  |
| `transcript.projectID` | string |  |
| `transcript.properties[].createdAt` | string |  |
| `transcript.properties[].default` | boolean |  |
| `transcript.properties[].id` | string |  |
| `transcript.properties[].metadata` | object |  |
| `transcript.properties[].name` | string |  |
| `transcript.properties[].type` | string |  |
| `transcript.properties[].updatedAt` | string |  |
| `transcript.properties[].value` | string |  |
| `transcript.recordingURL` | object |  |
| `transcript.sessionID` | string |  |
| `transcript.updatedAt` | string |  |

## Native endpoint

Through the native Voiceflow API, this operation is `GET https://analytics-api.voiceflow.com/v1/transcript/:transcriptId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcript.md) for the provider-specific parameters and requirements.

