# Feathery: List Emails Sent From Form



```
GET https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-emails-sent-from-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-emails-sent-from-form?connectionId=$CONNECTION_ID&form_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "form_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-emails-sent-from-form?${params}`, {
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
| `form_id` | string | yes | The ID of the form whose outbound emails you want to inspect. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start_time` | date | no | Only return emails sent after this time. |
| `end_time` | date | no | Only return emails sent before this time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "recipients": [
        "string"
      ],
      "subject": "string",
      "template_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | When the email was sent. |
| `recipients` | array<string> | The recipient addresses. |
| `subject` | string | The email subject. |
| `template_id` | string | The email template ID. |

## Native endpoint

Through the native Feathery API, this operation is `GET /api/logs/email/form/:form_id/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-emails-sent-from-form.md) for the provider-specific parameters and requirements.

