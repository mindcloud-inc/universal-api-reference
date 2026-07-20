# PrexView: Create document from XML

Creates a document in PrexView from XML data.

```
POST https://connect.mindcloud.co/v1/universal/prexView/latest/actions/create-document-from-xml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrexView `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prexView/latest/actions/create-document-from-xml" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "xml": "<hello>World</hello>",
  "template": "invoice-customer-{{Data._customer}}",
  "output": "pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prexView/latest/actions/create-document-from-xml', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "xml": "<hello>World</hello>",
    "template": "invoice-customer-{{Data._customer}}",
    "output": "pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xml` | string | yes | XML data to transform into the selected output format. Example: `<hello>World</hello>`. |
| `template` | string | yes | PrexView template name to use for document creation. Example: `invoice-customer-{{Data._customer}}`. |
| `output` | list<string> | yes | Document format to create: html, pdf, png, or jpg. One of: `HTML`, `JPG`, `PDF`, `PNG`. Default: `pdf`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateBackup` | string | no | Backup template name to use when the main template is unavailable. Example: `fallback-template`. |
| `note` | string | no | Optional metadata note for the transaction, up to 500 characters. Example: `Document: Invoice Customer: {{Data._customer}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "contentType": "string",
      "rateLimitLimit": 1,
      "rateLimitRemaining": 1,
      "rateLimitReset": 1,
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Rendered document content returned by PrexView. |
| `contentType` | string | MIME type of the rendered document. |
| `rateLimitLimit` | number | Total transaction limit from X-RateLimit-Limit. |
| `rateLimitRemaining` | number | Remaining transactions from X-RateLimit-Remaining. |
| `rateLimitReset` | number | Unix timestamp when transaction quota resets. |
| `transactionId` | string | PrexView transaction ID from the x-transaction-id response header. |

## Native endpoint

Through the native PrexView API, this operation is `POST /v1/transform` (base URL `https://api.prexview.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-from-xml.md) for the provider-specific parameters and requirements.

