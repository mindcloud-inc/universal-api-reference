# Resend: Get Template

Retrieves a template from Resend.

```
GET https://connect.mindcloud.co/v1/universal/resend/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resend/latest/actions/get-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resend/latest/actions/get-template?${params}`, {
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
| `id` | string | yes | Template identifier or alias. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "hasUnpublishedVersions": true,
      "html": "string",
      "id": "string",
      "name": "Ava Chen",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "replyTo": [
        "string"
      ],
      "status": "string",
      "subject": "string",
      "text": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | Template alias, when present. |
| `createdAt` | date | When the template was created. |
| `from` | string | Sender email address, when present. |
| `hasUnpublishedVersions` | boolean | Whether unpublished changes exist. |
| `html` | string | HTML content of the template. |
| `id` | string | Template identifier. |
| `name` | string | Template name. |
| `publishedAt` | date | When the template was published, when present. |
| `replyTo` | array<string> | Reply-to email addresses, when present. |
| `status` | string | Template publication status. |
| `subject` | string | Template subject line, when present. |
| `text` | string | Plain-text content of the template, when present. |
| `updatedAt` | date | When the template was last updated. |

## Native endpoint

Through the native Resend API, this operation is `GET /templates/:id` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

