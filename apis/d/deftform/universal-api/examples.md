# Deftform Universal API Examples

These examples use the MindCloud API key and Deftform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms

Retrieves forms and fields from Deftform.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-forms?${params}`, {
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
      "after_message": "string",
      "after_redirect_url": "https://example.com",
      "captcha": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "cta_label": "string",
      "description": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "is_closed": true,
      "name": "Ava Chen",
      "seo_description": "string",
      "seo_title": "string",
      "show_formtitle": true,
      "slug": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deftform/latest/actions/list-forms).

## Add Form Response

Creates a form response in Deftform.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deftform/latest/actions/add-form-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deftform/latest/actions/add-form-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "data": "[object Object]"
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Form Response action reference](actions/add-form-response.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deftform/latest/actions/add-form-response).
