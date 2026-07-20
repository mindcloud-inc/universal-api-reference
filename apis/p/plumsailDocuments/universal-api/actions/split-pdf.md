# Plumsail Documents: Split PDF

Splits a PDF in Plumsail Documents.

```
POST https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/split-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plumsail Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/split-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/split-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no | Default: `ExtractPages`. |
| `extractRange` | string | no |  |
| `pagesInChunk` | number | no |  |
| `chunksRange` | string | no |  |
| `bookmarkDepth` | number | no |  |
| `useBookmarksForFileNames` | boolean | no |  |
| `filenamePrefix` | string | no |  |
| `password` | string | no |  |
| `file` | file | no |  |
| `fileUrl` | string | no |  |
| `callbackUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | array<string> |  |

## Native endpoint

Through the native Plumsail Documents API, this operation is `POST /api/v2/pdf/split` (base URL `https://us-api.plumsail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-pdf.md) for the provider-specific parameters and requirements.

