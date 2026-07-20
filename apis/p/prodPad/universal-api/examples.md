# ProdPad Universal API Examples

These examples use the MindCloud API key and ProdPad connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Ideas

Retrieves ideas from ProdPad.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-ideas?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-ideas?${params}`, {
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
      "idea_count": 1,
      "ideas": [
        {
          "account": {
            "id": 1,
            "name": "Ava Chen",
            "slug": "string"
          },
          "actual_outcomes": "string",
          "confidence": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "creator": {
            "display_name": "Ava Chen",
            "id": 1,
            "username": "Ava Chen"
          },
          "description": "string",
          "engagement": 1,
          "id": 1,
          "impact": 1,
          "popularity": 1,
          "project_id": 1,
          "state": "string",
          "target_outcomes": "string",
          "title": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "uuid": "string",
          "web_url": "https://example.com"
        }
      ],
      "page": 1,
      "size": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Ideas action reference](actions/list-ideas.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/prodPad/latest/actions/list-ideas).

## Create Company

Creates a new company in ProdPad.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/create-company', {
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
      "city": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "size": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/prodPad/latest/actions/create-company).
