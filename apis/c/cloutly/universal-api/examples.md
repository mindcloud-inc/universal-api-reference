# Cloutly Universal API Examples

These examples use the MindCloud API key and Cloutly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Businesses

Retrieves businesses connected to your Cloutly account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/list-businesses?${params}`, {
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
      "coverPhotoUrl": "https://example.com",
      "id": "string",
      "logoSrc": "string",
      "name": "Ava Chen",
      "rating": "string",
      "sourceMap": [
        "string"
      ],
      "sources": [
        "string"
      ],
      "totalReviews": 1
    }
  ],
  "meta": {}
}
```

See the full [List Businesses action reference](actions/list-businesses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloutly/latest/actions/list-businesses).

## Create Business

Creates a new business in Cloutly.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/create-business" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/create-business', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Business action reference](actions/create-business.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloutly/latest/actions/create-business).
