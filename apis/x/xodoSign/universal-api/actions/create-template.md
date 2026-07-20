# Xodo Sign: Create Template

Creates a new template in Xodo Sign.

```
POST https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "business_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "business_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `business_id` | string | yes | The Xodo Sign business ID that owns the new template. |
| `is_draft` | string | no | Set to 1 to save the template as a draft. |
| `sandbox` | string | no | Set to 1 to enable sandbox mode for template creation. |
| `title` | string | no | Title for the template. |

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
| `created` | number | Unix timestamp when the template was created. |
| `document_hash` | string | Unique hash identifier of the created template. |
| `expires` | number | Unix timestamp when the template expires. |
| `files` | array<object> | Files attached to the template. |
| `is_cancelled` | number | 1 when the record is cancelled. |
| `is_completed` | number | 1 when the record is completed. |
| `is_draft` | number | 1 when the template is saved as a draft. |
| `is_template` | number | 1 when the record is a template. |
| `log` | array<object> | Template history entries. |
| `message` | string | Message stored with the template. |
| `meta` | array<object> | Additional metadata entries returned by Xodo Sign. |
| `recipients` | array<object> | Recipient roles configured on the template. |
| `requester_email` | string | Email address of the template requester. |
| `signers` | array<object> | Signer roles configured on the template. |
| `subject` | string | Subject of the template. |
| `template_id` | string | Template hash associated with the template when applicable. |
| `title` | string | Title of the template. |

## Native endpoint

Through the native Xodo Sign API, this operation is `POST /document` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

