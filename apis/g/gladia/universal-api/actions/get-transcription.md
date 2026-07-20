# Gladia: Get Transcription

Retrieves a transcription job's status, parameters, and result from Gladia.

```
GET https://connect.mindcloud.co/v1/universal/gladia/latest/actions/get-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gladia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gladia/latest/actions/get-transcription?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gladia/latest/actions/get-transcription?${params}`, {
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
| `id` | string | yes | Gladia transcription job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customMetadata": {},
      "errorCode": 1,
      "file": {},
      "id": "string",
      "kind": "string",
      "requestId": "string",
      "requestParams": {},
      "result": {},
      "status": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `customMetadata` | object |  |
| `errorCode` | number |  |
| `file` | object |  |
| `id` | string |  |
| `kind` | string |  |
| `requestId` | string |  |
| `requestParams` | object |  |
| `result` | object |  |
| `status` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Gladia API, this operation is `GET /v2/transcription/:id` (base URL `https://api.gladia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcription.md) for the provider-specific parameters and requirements.

