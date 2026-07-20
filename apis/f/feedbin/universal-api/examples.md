# Feedbin Universal API Examples

These examples use the MindCloud API key and Feedbin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Subscriptions

Retrieves a list of subscriptions from Feedbin.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-subscriptions?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "feed_id": 1,
      "feed_url": "https://example.com",
      "id": 1,
      "site_url": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Subscriptions action reference](actions/list-subscriptions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/feedbin/latest/actions/list-subscriptions).

## Create Saved Search

Creates a new saved search in Feedbin.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/create-saved-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/create-saved-search', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "query": "string"
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
      "name": "Ava Chen",
      "query": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Saved Search action reference](actions/create-saved-search.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/feedbin/latest/actions/create-saved-search).
