# Histre Universal API Examples

These examples use the MindCloud API key and Histre connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve User Settings

Retrieves user settings from Histre.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-user-settings?${params}`, {
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
      "email": "ava@example.com",
      "external_id": "string",
      "history": true,
      "org_name": "Ava Chen",
      "pagesize": 1,
      "plan": "string",
      "tz": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve User Settings action reference](actions/retrieve-user-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/histre/latest/actions/retrieve-user-settings).

## Add Notes to Collections

Adds notes to collections in Histre.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/histre/latest/actions/add-notes-to-collections" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urlItemItemIds[]": [
    "https://example.com"
  ],
  "bookIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/histre/latest/actions/add-notes-to-collections', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urlItemItemIds[]": ["https://example.com"],
    "bookIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Notes to Collections action reference](actions/add-notes-to-collections.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/histre/latest/actions/add-notes-to-collections).
