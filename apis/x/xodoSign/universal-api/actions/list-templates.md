# Xodo Sign: List Templates

Retrieves templates from Xodo Sign.

```
GET https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-templates?connectionId=$CONNECTION_ID&business_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "business_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-templates?${params}`, {
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
| `business_id` | string | yes | The Xodo Sign business ID to query templates from. |
| `limit` | string | no | Maximum number of templates to return. |
| `page` | string | no | Page number to return. |

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
| `document_hash` | string | Unique hash identifier of the template. |
| `expires` | number | Unix timestamp when the template expires. |
| `files` | array<object> | Files attached to the template. |
| `is_cancelled` | number | 1 when the record is cancelled. |
| `is_completed` | number | 1 when the record is completed. |
| `is_draft` | number | 1 when the template is saved as a draft. |
| `is_template` | number | 1 when the record is a template. |
| `log` | array<object> | History entries returned with the template. |
| `message` | string | Message stored on the template. |
| `meta` | array<object> | Additional metadata entries returned by Xodo Sign. |
| `recipients` | array<object> | Recipient roles configured on the template. |
| `requester_email` | string | Email address of the template requester. |
| `signers` | array<object> | Signer roles configured on the template. |
| `subject` | string | Subject of the template. |
| `template_id` | string | Template hash associated with the record when applicable. |
| `title` | string | Title of the template. |

## Native endpoint

Through the native Xodo Sign API, this operation is `GET /document` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

