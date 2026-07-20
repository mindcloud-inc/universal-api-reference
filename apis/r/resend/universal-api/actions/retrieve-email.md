# Resend: Retrieve Email

Retrieves an email from Resend.

```
GET https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-email?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-email?${params}`, {
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
| `id` | string | yes | Email identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bcc": [
        "string"
      ],
      "cc": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "html": "string",
      "id": "string",
      "lastEvent": "string",
      "object": "string",
      "replyTo": [
        "string"
      ],
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "subject": "string",
      "tags": [
        {}
      ],
      "text": "string",
      "to": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bcc` | array<string> | Blind carbon copy recipients. |
| `cc` | array<string> | Carbon copy recipients. |
| `createdAt` | date | When the email was created. |
| `from` | string | Sender email address. |
| `html` | string | HTML body of the email. |
| `id` | string | Email identifier. |
| `lastEvent` | string | Latest delivery lifecycle event. |
| `object` | string | Object type identifier. |
| `replyTo` | array<string> | Reply-to email addresses. |
| `scheduledAt` | date | Scheduled send time, when present. |
| `subject` | string | Email subject. |
| `tags` | array<object> | Email tags. |
| `text` | string | Plain-text body of the email. |
| `to` | array<string> | Recipient email addresses. |

## Native endpoint

Through the native Resend API, this operation is `GET /emails/:id` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-email.md) for the provider-specific parameters and requirements.

