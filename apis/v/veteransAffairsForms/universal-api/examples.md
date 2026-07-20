# Veterans Affairs Forms Universal API Examples

These examples use the MindCloud API key and Veterans Affairs Forms connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List VA Forms

Finds VA forms by number, keyword, or title.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteransAffairsForms/latest/actions/list-va-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veteransAffairsForms/latest/actions/list-va-forms?${params}`, {
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
      "attributes": {
        "benefit_categories": [
          {}
        ],
        "deleted_at": "2026-05-07T12:00:00.000Z",
        "first_issued_on": "2026-05-07T12:00:00.000Z",
        "form_details_url": "https://example.com",
        "form_name": "Ava Chen",
        "form_tool_intro": "string",
        "form_tool_url": "https://example.com",
        "form_type": "string",
        "form_usage": "string",
        "language": "string",
        "last_revision_on": "2026-05-07T12:00:00.000Z",
        "last_sha256_change": "2026-05-07T12:00:00.000Z",
        "pages": 1,
        "related_forms": [
          "string"
        ],
        "sha256": "string",
        "title": "string",
        "url": "https://example.com",
        "va_form_administration": "string",
        "valid_pdf": true
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List VA Forms action reference](actions/list-va-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/veteransAffairsForms/latest/actions/list-va-forms).
