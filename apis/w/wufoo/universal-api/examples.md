# Wufoo Universal API Examples

These examples use the MindCloud API key and Wufoo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms

Retrieves forms from Wufoo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-forms?${params}`, {
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
      "dateCreated": "string",
      "dateUpdated": "string",
      "description": "string",
      "email": "ava@example.com",
      "endDate": "string",
      "entryLimit": "string",
      "hash": "string",
      "isPublic": "string",
      "language": "string",
      "linkEntries": "https://example.com",
      "linkEntriesCount": "https://example.com",
      "linkFields": "https://example.com",
      "name": "Ava Chen",
      "redirectMessage": "string",
      "startDate": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wufoo/latest/actions/list-forms).

## Submit Form Entry

Creates a new entry in a specific Wufoo form.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/submit-form-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/submit-form-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string"
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
      "entryId": 1,
      "entryLink": "https://example.com",
      "success": 1
    }
  ],
  "meta": {}
}
```

See the full [Submit Form Entry action reference](actions/submit-form-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wufoo/latest/actions/submit-form-entry).
