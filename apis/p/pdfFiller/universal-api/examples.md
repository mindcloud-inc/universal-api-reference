# PdfFiller Universal API Examples

These examples use the MindCloud API key and PdfFiller connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates

Retrieves templates from PdfFiller.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "current_page": 1,
      "items": [
        {
          "created": 1,
          "fillable": true,
          "folder": {
            "folder_id": 1,
            "name": "Ava Chen"
          },
          "id": 1,
          "name": "Ava Chen",
          "status": "string",
          "type": "string",
          "updated": 1
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

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pdfFiller/latest/actions/list-templates).

## Create Fillable Form

Creates a fillable form in PdfFiller.

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

Example response:

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

See the full [Create Fillable Form action reference](actions/create-fillable-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pdfFiller/latest/actions/create-fillable-form).
