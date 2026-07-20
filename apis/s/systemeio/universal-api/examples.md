# Systeme.io Universal API Examples

These examples use the MindCloud API key and Systeme.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tags

Retrieves the collection of tags from Systeme.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-tags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-tags?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Tags action reference](actions/list-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/systemeio/latest/actions/list-tags).

## Add Contact Tag

Assigns a tag to a contact in Systeme.io.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/add-contact-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "tagId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/add-contact-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "tagId": 1
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
      "id": "string",
      "tagId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contact Tag action reference](actions/add-contact-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/systemeio/latest/actions/add-contact-tag).
