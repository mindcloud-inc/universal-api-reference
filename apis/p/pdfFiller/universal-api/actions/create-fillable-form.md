# PdfFiller: Create Fillable Form

Creates a fillable form in PdfFiller.

```
POST https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/create-fillable-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/create-fillable-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/create-fillable-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "access": "string",
      "additional_documents": [
        {
          "files": [
            {
              "date_created": "string",
              "filename": "Ava Chen",
              "id": 1,
              "ip": "string"
            }
          ],
          "name": "Ava Chen"
        }
      ],
      "allow_downloads": true,
      "callbacks": [
        {
          "callback_url": "https://example.com",
          "document_id": 1,
          "event_id": "string"
        }
      ],
      "custom_logo_id": 1,
      "custom_message": "string",
      "document_name": "Ava Chen",
      "email_required": true,
      "enforce_required_fields": true,
      "field_wizard": "string",
      "fillable_form_id": 1,
      "filled_forms_count": 1,
      "name_required": true,
      "notification_emails": [
        {
          "email": "ava@example.com",
          "name": "ava@example.com"
        }
      ],
      "notifications": "string",
      "redirect_url": "https://example.com",
      "reusable": true,
      "sender_notifications": true,
      "signature_stamp": true,
      "status": "string",
      "url": "https://example.com",
      "user_tokens": [
        {
          "org_id": 1,
          "token": "string",
          "url": "https://example.com",
          "user_id": 1
        }
      ],
      "welcome_screen": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `additional_documents[].files[].date_created` | string |  |
| `additional_documents[].files[].filename` | string |  |
| `additional_documents[].files[].id` | number |  |
| `additional_documents[].files[].ip` | string |  |
| `additional_documents[].name` | string |  |
| `allow_downloads` | boolean |  |
| `callbacks[].callback_url` | string |  |
| `callbacks[].document_id` | number |  |
| `callbacks[].event_id` | string |  |
| `custom_logo_id` | number |  |
| `custom_message` | string |  |
| `document_name` | string |  |
| `email_required` | boolean |  |
| `enforce_required_fields` | boolean |  |
| `field_wizard` | string |  |
| `fillable_form_id` | number |  |
| `filled_forms_count` | number |  |
| `name_required` | boolean |  |
| `notification_emails[].email` | string |  |
| `notification_emails[].name` | string |  |
| `notifications` | string |  |
| `redirect_url` | string |  |
| `reusable` | boolean |  |
| `sender_notifications` | boolean |  |
| `signature_stamp` | boolean |  |
| `status` | string |  |
| `url` | string |  |
| `user_tokens[].org_id` | number |  |
| `user_tokens[].token` | string |  |
| `user_tokens[].url` | string |  |
| `user_tokens[].user_id` | number |  |
| `welcome_screen` | boolean |  |

## Native endpoint

Through the native PdfFiller API, this operation is `POST /v2/fillable_forms` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fillable-form.md) for the provider-specific parameters and requirements.

