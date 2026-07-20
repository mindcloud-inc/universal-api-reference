# Handwrite Universal API Examples

These examples use the MindCloud API key and Handwrite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Handwritings

Retrieves handwritings from Handwrite.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/list-handwritings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/list-handwritings?${params}`, {
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
      "_id": "string",
      "name": "Ava Chen",
      "preview_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Handwritings action reference](actions/list-handwritings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/handwrite/latest/actions/list-handwritings).

## Send Batch Letters

Sends batch letters through Handwrite.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/send-batch-letters" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orders[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/send-batch-letters', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orders[]": [{}]
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
      "_id": "string",
      "card": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "environment": "string",
      "from": {},
      "handwriting": "string",
      "message": "string",
      "meta": {},
      "origin": "string",
      "proofs": [
        {}
      ],
      "status": "string",
      "to": {}
    }
  ],
  "meta": {}
}
```

See the full [Send Batch Letters action reference](actions/send-batch-letters.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/handwrite/latest/actions/send-batch-letters).
