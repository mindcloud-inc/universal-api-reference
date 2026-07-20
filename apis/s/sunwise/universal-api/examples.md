# Sunwise Universal API Examples

These examples use the MindCloud API key and Sunwise connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from Sunwise.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/list-contacts?${params}`, {
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
      "company_name": "Ava Chen",
      "created_at": "string",
      "emails": [
        {
          "email": "ava@example.com"
        }
      ],
      "id": "string",
      "name": "Ava Chen",
      "status_flag": "string",
      "telephones": [
        {
          "telephone": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sunwise/latest/actions/list-contacts).

## Bulk Create Projects No Files

Creates multiple projects without files in Sunwise.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/bulk-create-projects-no-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_id": "string",
  "project_names[]": [
    "Ava Chen"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/bulk-create-projects-no-files', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_id": "string",
    "project_names[]": ["Ava Chen"]
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
      "created_at": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Bulk Create Projects No Files action reference](actions/bulk-create-projects-no-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sunwise/latest/actions/bulk-create-projects-no-files).
