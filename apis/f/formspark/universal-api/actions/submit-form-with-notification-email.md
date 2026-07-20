# Formspark: Submit Form With Notification Email

Creates a Formspark form submission with notification email settings.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-notification-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-notification-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-notification-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The Formspark form ID or the special `echo` endpoint for validation. |
| `message` | string | no | Optional message field to include in the submission body. |
| `_email.subject` | string | no | Custom subject line for the notification email. |
| `_email.from` | string | no | Custom sender name for the notification email. |
| `_email.template.title` | string | no | Custom title for the default notification email template. |
| `_email.template.footer` | string | no | Set to false to hide the default notification email footer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_email": {
        "from": "ava@example.com",
        "subject": "ava@example.com",
        "template": {
          "footer": "ava@example.com",
          "title": "ava@example.com"
        }
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_email.from` | string | Notification email sender name override. |
| `_email.subject` | string | Notification email subject override. |
| `_email.template.footer` | string | Notification email footer visibility setting. |
| `_email.template.title` | string | Notification email template title override. |
| `message` | string | Echoed message field. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-notification-email.md) for the provider-specific parameters and requirements.

