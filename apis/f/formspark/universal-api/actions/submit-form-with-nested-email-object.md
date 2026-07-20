# Formspark: Submit Form With Nested Email Object

Creates a Formspark form submission with nested email settings.

```
POST https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-nested-email-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formspark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-nested-email-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "_email.subject": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formspark/latest/actions/submit-form-with-nested-email-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "_email.subject": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `message` | string | no | Submitted message body. |
| `_email.subject` | string | yes | Notification email subject inside the nested `_email` object. |
| `_email.from` | string | no | Sender display name inside the nested `_email` object. |
| `_email.template.title` | string | no | Title inside the nested `_email.template` object. |
| `_email.template.footer` | string | no | Footer toggle inside the nested `_email.template` object. |

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
| `_email.from` | string | Echoed nested email sender name. |
| `_email.subject` | string | Echoed nested email subject. |
| `_email.template.footer` | string | Echoed nested email template footer toggle. |
| `_email.template.title` | string | Echoed nested email template title. |
| `message` | string | Echoed message field. |

## Native endpoint

Through the native Formspark API, this operation is `POST :formId` (base URL `https://submit-form.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form-with-nested-email-object.md) for the provider-specific parameters and requirements.

