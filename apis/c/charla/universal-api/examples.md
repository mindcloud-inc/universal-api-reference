# Charla Universal API Examples

These examples use the MindCloud API key and Charla connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from Charla.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/charla/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/charla/latest/actions/list-contacts?${params}`, {
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
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "id": "string",
          "last_message_at": "2026-05-07T12:00:00.000Z",
          "last_seen_at": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "phone": "string"
        }
      ],
      "paging": {
        "has_next": true,
        "next_cursor": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/charla/latest/actions/list-contacts).

## Save Article

Saves an article record in Charla.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/charla/latest/actions/save-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/charla/latest/actions/save-article', {
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
      "article": "string",
      "categories": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "slug": "string",
      "status": "string",
      "title": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

See the full [Save Article action reference](actions/save-article.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/charla/latest/actions/save-article).
