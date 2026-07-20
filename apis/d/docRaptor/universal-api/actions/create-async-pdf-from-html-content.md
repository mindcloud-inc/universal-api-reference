# DocRaptor: Create Async PDF from HTML Content

Creates an async PDF in DocRaptor from HTML content.

```
POST https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/create-async-pdf-from-html-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocRaptor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/create-async-pdf-from-html-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/create-async-pdf-from-html-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentContent` | string | yes | HTML content to convert into an async PDF. |
| `name` | string | no | Optional output file name. |
| `test` | boolean | no | Create a watermarked test document instead of a production document. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Optional URL DocRaptor should call when the async job completes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status_id` | string | ID used to check async document status. |

## Native endpoint

Through the native DocRaptor API, this operation is `POST /docs` (base URL `https://api.docraptor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-async-pdf-from-html-content.md) for the provider-specific parameters and requirements.

