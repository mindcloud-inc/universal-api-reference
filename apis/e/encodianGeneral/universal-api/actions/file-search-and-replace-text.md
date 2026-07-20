# Encodian - General: File Search And Replace Text

Searches and replaces text in a file.

```
PUT https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/file-search-and-replace-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - General `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/file-search-and-replace-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Phrases": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/file-search-and-replace-text', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Phrases": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `FileName` | string | no | Source filename including extension. |
| `FileContent` | string | no | Base64-encoded source file content. |
| `Phrases` | list<object> | yes | Array of search and replacement phrase objects. Example: `[object Object]`. |

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

Through the native Encodian - General API, this operation is `POST /api/v1/General/SearchAndReplaceText` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/file-search-and-replace-text.md) for the provider-specific parameters and requirements.

