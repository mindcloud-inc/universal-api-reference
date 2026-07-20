# Encodian - General: AI Translate File

Translates a file to a target language with Encodian AI.

```
POST https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/ai-translate-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - General `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/ai-translate-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen",
  "fileContent": "string",
  "targetLanguage": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/ai-translate-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen",
    "fileContent": "string",
    "targetLanguage": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | yes | Source filename including extension. |
| `fileContent` | string | yes | Base64-encoded source file content. |
| `targetLanguage` | string | yes | Language to translate the file into. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "FileContent": "string",
      "Filename": "Ava Chen",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> |  |
| `FileContent` | string |  |
| `Filename` | string |  |
| `HttpStatusCode` | number |  |
| `HttpStatusMessage` | string |  |
| `OperationId` | string |  |
| `OperationStatus` | string |  |

## Native endpoint

Through the native Encodian - General API, this operation is `POST /api/v1/General/AITranslateFile` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ai-translate-file.md) for the provider-specific parameters and requirements.

