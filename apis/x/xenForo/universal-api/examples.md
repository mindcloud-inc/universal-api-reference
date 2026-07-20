# XenForo Universal API Examples

These examples use the MindCloud API key and XenForo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Site Info

Retrieves site and API information from XenForo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-site-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-site-info?${params}`, {
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
      "api_url": "https://example.com",
      "base_url": "https://example.com",
      "key[allow_all_scopes]": true,
      "key[scopes]": [
        "string"
      ],
      "key[type]": "string",
      "key[user_id]": 1,
      "site_title": "string",
      "version_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Site Info action reference](actions/get-site-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xenForo/latest/actions/get-site-info).

## Add Thread Reply

Creates a reply post in XenForo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/add-thread-reply" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "threadId": "123",
  "message": "Thanks for the update."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/add-thread-reply', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "threadId": "123",
    "message": "Thanks for the update."
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
      "post": {
        "message": "string",
        "post_date": 1,
        "post_id": 1,
        "thread_id": 1,
        "user_id": 1,
        "username": "Ava Chen",
        "view_url": "https://example.com"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Thread Reply action reference](actions/add-thread-reply.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xenForo/latest/actions/add-thread-reply).
