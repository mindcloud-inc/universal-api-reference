# MailerSend: Get Bulk Email Status



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-bulk-email-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-bulk-email-status?connectionId=$CONNECTION_ID&bulkEmailId=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bulkEmailId": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-bulk-email-status?${params}`, {
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
| `bulkEmailId` | string | yes | ID of the MailerSend bulk email job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "messagesId": "string",
      "state": "string",
      "suppressedRecipients": [
        {}
      ],
      "suppressedRecipientsCount": 1,
      "totalRecipientsCount": 1,
      "updatedAt": "string",
      "validationErrors": [
        {}
      ],
      "validationErrorsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Bulk email job creation timestamp. |
| `id` | string | MailerSend bulk email job ID. |
| `messagesId` | string | Serialized message ID collection returned by MailerSend. |
| `state` | string | Processing state of the bulk email job. |
| `suppressedRecipients` | array<object> | Suppressed recipient records when present. |
| `suppressedRecipientsCount` | number | Number of suppressed recipients. |
| `totalRecipientsCount` | number | Total recipients in the bulk email job. |
| `updatedAt` | string | Bulk email job update timestamp. |
| `validationErrors` | array<object> | Validation error records when present. |
| `validationErrorsCount` | number | Number of validation errors in the bulk email job. |

## Native endpoint

Through the native MailerSend API, this operation is `GET /bulk-email/:bulk_email_id` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-email-status.md) for the provider-specific parameters and requirements.

