# PlatoForms Universal API Examples

These examples use the MindCloud API key and PlatoForms connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms

Retrieves a list of forms from PlatoForms.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-forms?${params}`, {
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
      "created_date": "2026-05-07T12:00:00.000Z",
      "current_version_submission": "string",
      "folder": {},
      "id": "string",
      "is_published": "string",
      "modified_date": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pdf": {},
      "published_url": "https://example.com",
      "published_version": "string",
      "total_submission": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/platoForms/latest/actions/list-forms).

## Create Form

Creates a new form in PlatoForms.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form_identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form_identifier": "string"
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
      "field_detection_method": "string",
      "folder_id": "string",
      "form_name": "Ava Chen",
      "form_status": "string",
      "form_type": "string",
      "id": "string",
      "pdf_name": "Ava Chen",
      "pdf_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Form action reference](actions/create-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/platoForms/latest/actions/create-form).
