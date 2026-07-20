# DocMaker: Create Webpage PDF With Metadata

Creates a webpage PDF with metadata in DocMaker.

```
POST https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/create-webpage-pdf-with-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocMaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/create-webpage-pdf-with-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com",
  "pageSize": "string",
  "landscape": true,
  "metadata": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/create-webpage-pdf-with-metadata', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com",
    "pageSize": "string",
    "landscape": true,
    "metadata": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `url` | string | yes |  |
| `pageSize` | string | yes |  |
| `landscape` | boolean | yes |  |
| `metadata` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | The DocMaker job identifier. |
| `status` | string | The initial DocMaker job status. |

## Native endpoint

Through the native DocMaker API, this operation is `POST /page_pdf` (base URL `https://api.v2.docmaker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webpage-pdf-with-metadata.md) for the provider-specific parameters and requirements.

