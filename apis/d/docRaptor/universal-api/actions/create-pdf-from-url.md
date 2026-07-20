# DocRaptor: Create PDF from URL

Creates a PDF in DocRaptor from a URL.

```
POST https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/create-pdf-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocRaptor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/create-pdf-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/create-pdf-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentUrl` | string | yes | Public URL of the page DocRaptor should convert. |
| `name` | string | no | Optional output file name. |
| `test` | boolean | no | Create a watermarked test document instead of a production document. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DocRaptor API returns.

## Native endpoint

Through the native DocRaptor API, this operation is `POST /docs` (base URL `https://api.docraptor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf-from-url.md) for the provider-specific parameters and requirements.

