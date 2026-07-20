# Document AI: Split Document



```
GET https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/split-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/split-document?connectionId=$CONNECTION_ID&InputFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "InputFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/split-document?${params}`, {
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
| `InputFile` | file | yes | Document file to split. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recognitionMode` | string | no | Optional recognition mode sent as a request header. Default: `Advanced`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subDocuments": [
        {}
      ],
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subDocuments` | array<object> | Split subdocuments. |
| `successful` | boolean | Whether document splitting succeeded. |

## Native endpoint

Through the native Document AI API, this operation is `POST /document-ai/document/extract/split` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-document.md) for the provider-specific parameters and requirements.

