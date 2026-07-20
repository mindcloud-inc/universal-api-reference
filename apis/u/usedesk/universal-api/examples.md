# Usedesk Universal API Examples

These examples use the MindCloud API key and Usedesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Channels

Retrieves a list of channels from Usedesk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-channels?${params}`, {
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
      "channel_id": 1,
      "channel_name": "Ava Chen",
      "channel_type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Channels action reference](actions/list-channels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/usedesk/latest/actions/list-channels).

## Add Article Rating

Adds a rating to a knowledge base article in Usedesk.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/add-article-rating" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "articleId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/add-article-rating', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "articleId": 1
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
      "rating": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Article Rating action reference](actions/add-article-rating.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/usedesk/latest/actions/add-article-rating).
