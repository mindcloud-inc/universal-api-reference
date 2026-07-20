# Xodo Sign: Get Document or Template

Retrieves a document or template from Xodo Sign.

```
GET https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/get-document-or-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/get-document-or-template?connectionId=$CONNECTION_ID&business_id=string&document_hash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "business_id": "string",
  "document_hash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/get-document-or-template?${params}`, {
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
| `business_id` | string | yes | The Xodo Sign business ID that owns the document or template. |
| `document_hash` | string | yes | The unique document or template hash to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "document_hash": "string",
      "expires": 1,
      "files": [
        {}
      ],
      "is_cancelled": 1,
      "is_completed": 1,
      "is_draft": 1,
      "is_template": 1,
      "log": [
        {}
      ],
      "message": "string",
      "meta": [
        {}
      ],
      "recipients": [
        {}
      ],
      "requester_email": "ava@example.com",
      "signers": [
        {}
      ],
      "subject": "string",
      "template_id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Unix timestamp when the document was created. |
| `document_hash` | string | Unique hash identifier of the document or template. |
| `expires` | number | Unix timestamp when the document expires. |
| `files` | array<object> | Files attached to the document or template. |
| `is_cancelled` | number | 1 when the document is cancelled, otherwise 0. |
| `is_completed` | number | 1 when the document is completed, otherwise 0. |
| `is_draft` | number | 1 when the document is a draft, otherwise 0. |
| `is_template` | number | 1 when the record is a template, otherwise 0. |
| `log` | array<object> | Document history entries. |
| `message` | string | Message sent with the document or template. |
| `meta` | array<object> | Additional metadata entries returned by Xodo Sign. |
| `recipients` | array<object> | Recipients associated with the document or template. |
| `requester_email` | string | Email address of the document requester. |
| `signers` | array<object> | Signers associated with the document or template. |
| `subject` | string | Subject of the document or template. |
| `template_id` | string | Template hash associated with the document when applicable. |
| `title` | string | Title of the document or template. |

## Native endpoint

Through the native Xodo Sign API, this operation is `GET /document` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-or-template.md) for the provider-specific parameters and requirements.

