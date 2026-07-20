# PdfFiller: List Fillable Forms

Retrieves fillable forms from PdfFiller.

```
GET https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-fillable-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-fillable-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-fillable-forms?${params}`, {
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
      "current_page": 1,
      "items": [
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
      "next_page_url": "https://example.com",
      "per_page": 1,
      "prev_page_url": "https://example.com",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number |  |
| `items[].access` | string |  |
| `items[].additional_documents[].files[].date_created` | string |  |
| `items[].additional_documents[].files[].filename` | string |  |
| `items[].additional_documents[].files[].id` | number |  |
| `items[].additional_documents[].files[].ip` | string |  |
| `items[].additional_documents[].name` | string |  |
| `items[].allow_downloads` | boolean |  |
| `items[].callbacks[].callback_url` | string |  |
| `items[].callbacks[].document_id` | number |  |
| `items[].callbacks[].event_id` | string |  |
| `items[].custom_logo_id` | number |  |
| `items[].custom_message` | string |  |
| `items[].document_name` | string |  |
| `items[].email_required` | boolean |  |
| `items[].enforce_required_fields` | boolean |  |
| `items[].field_wizard` | string |  |
| `items[].fillable_form_id` | number |  |
| `items[].filled_forms_count` | number |  |
| `items[].name_required` | boolean |  |
| `items[].notification_emails[].email` | string |  |
| `items[].notification_emails[].name` | string |  |
| `items[].notifications` | string |  |
| `items[].redirect_url` | string |  |
| `items[].reusable` | boolean |  |
| `items[].sender_notifications` | boolean |  |
| `items[].signature_stamp` | boolean |  |
| `items[].status` | string |  |
| `items[].url` | string |  |
| `items[].user_tokens[].org_id` | number |  |
| `items[].user_tokens[].token` | string |  |
| `items[].user_tokens[].url` | string |  |
| `items[].user_tokens[].user_id` | number |  |
| `items[].welcome_screen` | boolean |  |
| `next_page_url` | string |  |
| `per_page` | number |  |
| `prev_page_url` | string |  |
| `total` | number |  |

## Native endpoint

Through the native PdfFiller API, this operation is `GET /v2/fillable_forms` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fillable-forms.md) for the provider-specific parameters and requirements.

