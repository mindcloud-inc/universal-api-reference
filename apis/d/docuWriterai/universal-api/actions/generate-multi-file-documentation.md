# DocuWriter.ai: Generate Multi-File Documentation



```
POST https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/generate-multi-file-documentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/generate-multi-file-documentation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files[]": [
    {}
  ],
  "files[].filename": "Ava Chen",
  "files[].source_code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/generate-multi-file-documentation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files[]": [{}],
    "files[].filename": "Ava Chen",
    "files[].source_code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files[]` | array<object> | yes | Array of file objects. |
| `files[].filename` | string | yes | Name of one source file. |
| `files[].source_code` | string | yes | Source code for one file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "generation": "string",
      "markdown": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Rendered content output. |
| `generation` | string | Generated multi-file documentation content. |
| `markdown` | string | Markdown version of the generated documentation. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `POST /api/generate-multi-file-documentation` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-multi-file-documentation.md) for the provider-specific parameters and requirements.

