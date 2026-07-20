# Tellephant Universal API Examples

These examples use the MindCloud API key and Tellephant connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List incoming logs

Retrieves incoming message logs from Tellephant.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/list-incoming-logs?connectionId=$CONNECTION_ID&startDate=24-04-2026&endDate=24-04-2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "24-04-2026",
  "endDate": "24-04-2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/list-incoming-logs?${params}`, {
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
      "channel": "string",
      "contact_id": "string",
      "content_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "media_url": "https://example.com",
      "message_type": "string",
      "sender_name": "Ava Chen",
      "text": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

See the full [List incoming logs action reference](actions/list-incoming-logs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tellephant/latest/actions/list-incoming-logs).

## Create tags

Creates tags for contacts in Tellephant.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/create-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/create-tags', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}]
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
      "error": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create tags action reference](actions/create-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tellephant/latest/actions/create-tags).
