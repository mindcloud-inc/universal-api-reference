# Typeflo Universal API Examples

These examples use the MindCloud API key and Typeflo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Authors

Retrieves author profiles from the Typeflo site.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/list-authors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/list-authors?${params}`, {
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
      "avatar": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "metadescription": "string",
      "name": "Ava Chen",
      "slug": "string",
      "socials": {}
    }
  ],
  "meta": {}
}
```

See the full [List Authors action reference](actions/list-authors.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typeflo/latest/actions/list-authors).

## Create Category

Creates a new category in Typeflo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/create-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Category action reference](actions/create-category.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typeflo/latest/actions/create-category).
