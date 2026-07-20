# Encodian - General: AI Process Mortgage Document US

Extracts US mortgage document data with Encodian AI.

```
GET https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/ai-process-mortgage-document-us
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - General `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/ai-process-mortgage-document-us?connectionId=$CONNECTION_ID&fileContent=string&processFileMortgageModel=Mortgage1003" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string",
  "processFileMortgageModel": "Mortgage1003"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/ai-process-mortgage-document-us?${params}`, {
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
| `fileContent` | string | yes | Base64-encoded source file content. |
| `processFileMortgageModel` | string | yes | Select the Encodian mortgage document model to use. Example: `Mortgage1003`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> |  |
| `HttpStatusCode` | number |  |
| `HttpStatusMessage` | string |  |
| `OperationId` | string |  |
| `OperationStatus` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Encodian - General API, this operation is `POST /api/v1/General/AIProcessMortgageUS` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ai-process-mortgage-document-us.md) for the provider-specific parameters and requirements.

