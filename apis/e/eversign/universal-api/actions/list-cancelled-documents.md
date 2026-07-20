# Eversign: List Cancelled Documents

Retrieves cancelled documents from your Eversign account.

```
GET https://connect.mindcloud.co/v1/universal/eversign/latest/actions/list-cancelled-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eversign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eversign/latest/actions/list-cancelled-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eversign/latest/actions/list-cancelled-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "client": "string",
      "completed": "string",
      "created": 1,
      "custom_requester_email": "ava@example.com",
      "custom_requester_name": "Ava Chen",
      "document_hash": "string",
      "embedded": 1,
      "embedded_signing_enabled": 1,
      "enable_signature_frame": 1,
      "expires": 1,
      "fields": [
        [
          "string"
        ]
      ],
      "files": [
        {}
      ],
      "flexible_signing": 1,
      "in_person": 1,
      "is_archived": 1,
      "is_cancelled": 1,
      "is_completed": 1,
      "is_deleted": 1,
      "is_draft": 1,
      "is_expired": 1,
      "is_template": 1,
      "is_trashed": 1,
      "log": [
        {}
      ],
      "message": "string",
      "meta": [
        "string"
      ],
      "permission": "string",
      "recipients": [
        "string"
      ],
      "redirect": "string",
      "redirect_decline": "string",
      "reminders": 1,
      "requester_email": "ava@example.com",
      "require_all_signers": 1,
      "signers": [
        {}
      ],
      "subject": "string",
      "template_id": "string",
      "title": "string",
      "use_signer_order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | string |  |
| `completed` | string |  |
| `created` | number |  |
| `custom_requester_email` | string |  |
| `custom_requester_name` | string |  |
| `document_hash` | string |  |
| `embedded` | number |  |
| `embedded_signing_enabled` | number |  |
| `enable_signature_frame` | number |  |
| `expires` | number |  |
| `fields` | array<array> |  |
| `files` | array<object> |  |
| `flexible_signing` | number |  |
| `in_person` | number |  |
| `is_archived` | number |  |
| `is_cancelled` | number |  |
| `is_completed` | number |  |
| `is_deleted` | number |  |
| `is_draft` | number |  |
| `is_expired` | number |  |
| `is_template` | number |  |
| `is_trashed` | number |  |
| `log` | array<object> |  |
| `message` | string |  |
| `meta` | array |  |
| `permission` | string |  |
| `recipients` | array |  |
| `redirect` | string |  |
| `redirect_decline` | string |  |
| `reminders` | number |  |
| `requester_email` | string |  |
| `require_all_signers` | number |  |
| `signers` | array<object> |  |
| `subject` | string |  |
| `template_id` | string |  |
| `title` | string |  |
| `use_signer_order` | number |  |

## Native endpoint

Through the native Eversign API, this operation is `GET /document` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cancelled-documents.md) for the provider-specific parameters and requirements.

