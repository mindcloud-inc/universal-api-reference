# Encodian - General: Archive Extract

Extracts files from a ZIP archive in Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/archive-extract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - General `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/archive-extract?connectionId=$CONNECTION_ID&fileContent=string&includeFolders=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string",
  "includeFolders": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/archive-extract?${params}`, {
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
| `fileContent` | string | yes | Base64-encoded archive file content. |
| `includeFolders` | boolean | yes | Whether to include folder entries in the extracted output. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {}
      ],
      "Errors": [
        "string"
      ],
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
| `documents` | array<object> |  |
| `Errors` | array<string> |  |
| `HttpStatusCode` | number |  |
| `HttpStatusMessage` | string |  |
| `OperationId` | string |  |
| `OperationStatus` | string |  |

## Native endpoint

Through the native Encodian - General API, this operation is `POST /api/v1/General/ExtractFromArchive` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-extract.md) for the provider-specific parameters and requirements.

