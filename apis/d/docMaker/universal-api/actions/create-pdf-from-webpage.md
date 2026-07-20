# DocMaker: Create PDF from Webpage

Creates a PDF from a webpage in DocMaker.

```
POST https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/create-pdf-from-webpage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocMaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/create-pdf-from-webpage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com",
  "pageSize": "string",
  "landscape": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/create-pdf-from-webpage', {
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
    "landscape": true
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
| `loadTime` | number | no |  |
| `pageRanges` | string | no |  |
| `getBase64` | boolean | no |  |
| `landscape` | boolean | yes |  |
| `marginLeft` | string | no |  |
| `marginRight` | string | no |  |
| `marginTop` | string | no |  |
| `marginBottom` | string | no |  |
| `timeZone` | string | no |  |
| `language` | string | no |  |
| `vWidth` | number | no |  |
| `vHeight` | number | no |  |
| `showFooter` | string | no |  |
| `htmlFooter` | string | no |  |
| `uploadOutputFile` | boolean | no |  |
| `metadata` | string | no |  |
| `webhookUrl` | string | no |  |
| `webhookObjectId` | string | no |  |
| `webhookObjectType` | string | no |  |

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
| `jobId` | string | DocMaker job identifier for the created PDF request |
| `status` | string | DocMaker job creation status |

## Native endpoint

Through the native DocMaker API, this operation is `POST /page_pdf` (base URL `https://api.v2.docmaker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf-from-webpage.md) for the provider-specific parameters and requirements.

