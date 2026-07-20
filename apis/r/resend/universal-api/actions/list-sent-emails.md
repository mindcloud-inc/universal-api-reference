# Resend: List Sent Emails

Retrieves sent emails from Resend.

```
GET https://connect.mindcloud.co/v1/universal/resend/latest/actions/list-sent-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resend/latest/actions/list-sent-emails?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resend/latest/actions/list-sent-emails?${params}`, {
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
      "bcc": [
        "string"
      ],
      "cc": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "id": "string",
      "lastEvent": "string",
      "replyTo": [
        "string"
      ],
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "subject": "string",
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
| `id` | string | Email identifier. |
| `lastEvent` | string | Latest delivery lifecycle event. |
| `replyTo` | array<string> | Reply-to email addresses. |
| `scheduledAt` | date | Scheduled send time, when present. |
| `subject` | string | Email subject. |
| `to` | array<string> | Recipient email addresses. |

## Native endpoint

Through the native Resend API, this operation is `GET /emails` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sent-emails.md) for the provider-specific parameters and requirements.

