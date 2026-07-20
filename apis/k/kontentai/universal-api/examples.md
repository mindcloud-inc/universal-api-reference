# Kontent.ai Universal API Examples

These examples use the MindCloud API key and Kontent.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List management languages

Retrieves languages from your Kontent.ai environment.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-management-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-management-languages?${params}`, {
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
      "codename": "Ava Chen",
      "id": "string",
      "is_default": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List management languages action reference](actions/list-management-languages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kontentai/latest/actions/list-management-languages).

## Add content type snippet

Creates a new content type snippet in Kontent.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/add-content-type-snippet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/add-content-type-snippet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
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
      "codename": "Ava Chen",
      "elements": [
        {
          "codename": "Ava Chen",
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add content type snippet action reference](actions/add-content-type-snippet.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kontentai/latest/actions/add-content-type-snippet).
