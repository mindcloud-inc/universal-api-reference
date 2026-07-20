# Readwise Universal API Examples

These examples use the MindCloud API key and Readwise connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Connection

Validates the connected Readwise access token.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/validate-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/validate-connection?${params}`, {
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
      "authenticated": true,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Connection action reference](actions/validate-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/readwise/latest/actions/validate-connection).

## Add Book Tag

Creates a new tag for a Readwise book.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/add-book-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readwise/latest/actions/add-book-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookId": 1,
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
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add Book Tag action reference](actions/add-book-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/readwise/latest/actions/add-book-tag).
